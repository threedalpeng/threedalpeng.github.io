<script lang="ts">
	import PptxIFrame from '$lib/presentations/PptxIFrame.svelte';
	import presentations from '$lib/presentations/model';

	let currentIndex = $state<number>(0);

	function changeCurrentIndex(idx: number) {
		currentIndex = idx;
	}
</script>

<div class="flex h-screen flex-row">
	<PptxIFrame title={presentations[currentIndex].title} link={presentations[currentIndex].link}
	></PptxIFrame>
	<div class="flex w-80 flex-col bg-stone-800 text-white">
		<div class="flex flex-1 flex-col bg-stone-500 font-bold">
			{#each presentations as pt, idx}
				<button class="p-4 text-left hover:bg-stone-600" onclick={() => changeCurrentIndex(idx)}>
					{pt.title}
				</button>
			{/each}
		</div>
		<div class="p-4">
			<h1 class="font-semibold">코멘트</h1>
			<p>{presentations[currentIndex].description}</p>
		</div>
		<div class="bg-stone-500">
			<a href="/">
				<button class="w-full p-4 font-bold hover:bg-stone-600">← 메인으로 돌아가기 </button></a
			>
		</div>
	</div>
</div>
