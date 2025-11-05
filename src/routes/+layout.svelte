<script>
	import '../app.css';
	import favicon from '$lib/assets/white_crab.png';
	
	let { children } = $props();
</script>

<svelte:head>
	<title>DocForge Documentation Co-Pilot</title>
	<meta name="description" content="AI-powered documentation that stays in sync with your code changes." />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<link rel="icon" href={favicon} />
	
	<!-- Open Graph / Facebook -->
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://docforge.com/" />
	<meta property="og:title" content="DocForge - AI Documentation Generation for Codebases" />
	<meta property="og:description" content="DocForge generates and maintains documentation for your codebase automatically. AI-powered documentation that stays in sync with your code changes." />
	<meta property="og:image" content="https://docforge.com/white_crab.jpg" />

	<!-- Twitter -->
	<meta property="twitter:card" content="summary_large_image" />
	<meta property="twitter:url" content="https://docforge.com/" />
	<meta property="twitter:title" content="DocForge - AI Documentation Generation for Codebases" />
	<meta property="twitter:description" content="DocForge generates and maintains documentation for your codebase automatically. AI-powered documentation that stays in sync with your code changes." />
	<meta property="twitter:image" content="https://docforge.com/white_crab.jpg" />
</svelte:head>

{@render children?.()}
