<script lang="ts">
	import PptxIFrame from '../../lib/presentations/PptxIFrame.svelte';
	import presentations from '$lib/presentations/model';


	let currentIndex = 0;

	function changeCurrentIndex(idx: number) {
		currentIndex = idx;
	}
    
</script>

<div class="flex flex-row h-screen">
	<PptxIFrame title={presentations[currentIndex].title} link={presentations[currentIndex].link}
	></PptxIFrame>
	<div class="flex flex-col w-80 bg-stone-800 text-white">
		<div class="flex flex-col flex-1 bg-stone-500 font-bold">
			{#each presentations as pt, idx}
				<button class="text-left hover:bg-stone-600 p-4" on:click={() => changeCurrentIndex(idx)}>
					{pt.title}
				</button>
			{/each}
		</div>
		<div class="p-4">
			<h1 class="font-semibold">코멘트</h1>
			<p>{presentations[currentIndex].description}</p>
		</div>
		<div class="bg-stone-500">
			<a href="/"> <button class="font-bold p-4 w-full hover:bg-stone-600">← 메인으로 돌아가기 </button></a>
		</div>
	</div>
</div>
