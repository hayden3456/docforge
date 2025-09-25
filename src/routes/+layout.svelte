<script>
	import '../app.css';
	import favicon from '$lib/assets/white_crab.png';
	
	let { children } = $props();
</script>

<svelte:head>
	<title>DocForge</title>
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}
