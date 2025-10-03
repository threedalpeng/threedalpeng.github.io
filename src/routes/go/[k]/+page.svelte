<script lang="ts">
	// 클라이언트 전용 + 정적 프리렌더
	export const ssr = false;
	export const prerender = true;

	import { onMount } from 'svelte';
	import { base } from '$app/paths';
	import { page } from '$app/stores';
	import { get } from 'svelte/store';

	let url = '';
	let error = '';
	const { k } = get(page).params; // /go/[k] 에서 받은 키

	onMount(async () => {
		try {
			const res = await fetch(`${base}/links.json?t=${Date.now()}`, { cache: 'no-store' });
			if (!res.ok) throw new Error(`links.json load failed (${res.status})`);
			const links = await res.json();
			url = (links?.[k] ?? '').trim();
			if (!url) throw new Error(`No target for key "${k}"`);

			// 히스토리 교체(뒤로가기 시 /go/[k]로 안 돌아오게)
			window.location.replace(url);
		} catch (e) {
			error = e instanceof Error ? e.message : String(e);
			console.error(e);
		}
	});
</script>

<svelte:head>
	<title>Redirecting…</title>
	<meta name="robots" content="noindex" />
</svelte:head>

<div
	style="min-height:100vh;display:grid;place-items:center;font-family:system-ui,-apple-system,Segoe UI,Roboto,sans-serif;"
>
	{#if error}
		<div style="max-width:640px;padding:1rem;text-align:center;">
			<p><code>{k}</code> 키의 목적지를 찾지 못했어요.</p>
			<p><code>static/links.json</code>에 <code>"{k}": "https://…"</code> 형태로 추가해 주세요.</p>
			<pre
				style="white-space:pre-wrap;background:#f6f6f6;padding:.5rem;border-radius:.5rem;">{error}</pre>
		</div>
	{:else}
		<div style="max-width:640px;padding:1rem;text-align:center;">
			<p>이동 중… 잠시만요.</p>
			{#if url}
				<p>자동 이동이 안 되면 <a rel="nofollow" href={url}>{url}</a>를 눌러 주세요.</p>
			{/if}
		</div>
	{/if}
</div>
