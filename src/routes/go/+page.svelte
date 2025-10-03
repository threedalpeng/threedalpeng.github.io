<script lang="ts">
	// 클라이언트 전용 + 정적 프리렌더 가능(동적 경로 없음)
	export const ssr = false;
	export const prerender = true;

	import { onMount } from 'svelte';
	import { base } from '$app/paths';

	let url = '';
	let error = '';
	let k = '';
	let available: string[] = [];

	async function loadLinks() {
		const res = await fetch(`${base}/links.json?t=${Date.now()}`, { cache: 'no-store' });
		if (!res.ok) throw new Error(`links.json load failed (${res.status})`);
		return (await res.json()) as Record<string, string>;
	}

	onMount(async () => {
		try {
			const u = new URL(window.location.href);
			k = (u.searchParams.get('k') ?? '').trim();

			const links = await loadLinks();
			available = Object.keys(links).sort();

			if (!k) throw new Error('Missing ?k=<key>');
			url = (links[k] ?? '').trim();
			if (!url) throw new Error(`No target for key "${k}"`);

			// 히스토리 교체(뒤로가기 시 /go로 안 돌아오게)
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

{#if error}
	<div
		style="min-height:100vh;display:grid;place-items:center;font-family:system-ui,-apple-system,Segoe UI,Roboto,sans-serif;"
	>
		<div style="max-width:720px;padding:1rem;text-align:center;">
			<p style="margin:0 0 .5rem 0;">단축 링크를 처리하지 못했습니다.</p>
			<p style="margin:.25rem 0;color:#c00;"><code>{error}</code></p>
			<p style="margin:1rem 0 0 0;">형식: <code>/go?k=&lt;key&gt;</code></p>
			{#if available.length}
				<p style="margin:.5rem 0 0 0;">등록된 키:</p>
				<div
					style="display:flex;flex-wrap:wrap;gap:.5rem;justify-content:center;margin-top:.25rem;"
				>
					{#each available as key}
						<a
							href={`?k=${encodeURIComponent(key)}`}
							style="padding:.25rem .5rem;border:1px solid #ddd;border-radius:.5rem;text-decoration:none;"
						>
							{key}
						</a>
					{/each}
				</div>
			{/if}
		</div>
	</div>
{/if}
