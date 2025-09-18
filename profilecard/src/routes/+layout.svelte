<script>
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon}/>
	<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap">
</svelte:head>

{@render children?.()}
