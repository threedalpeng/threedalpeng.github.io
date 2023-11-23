<script lang="ts">
	export let title: string;
	export let link: string;
</script>

<iframe {title} src={link} frameBorder="0" class="h-full flex-1">
	포함된{' '}
	<a target="_blank" href="https://office.com"> Microsoft Office </a>{' '}
	프레젠테이션, 제공:{' '}
	<a target="_blank" href="https://office.com/webapps"> Office </a>
</iframe>
