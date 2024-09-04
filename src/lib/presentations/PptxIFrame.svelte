<script lang="ts">
	interface PptxIFrameProps {
		title: string;
		link: string;
	}
	let { title, link }: PptxIFrameProps = $props();
</script>

<iframe {title} src={link} class="h-full flex-1" frameborder="0" scrolling="no"></iframe>
