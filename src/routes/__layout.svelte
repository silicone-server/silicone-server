<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import Footer from "../lib/components/Footer.svelte";
	import '../app.css';
</script>

<svelte:head>
	<title>Silicone Server</title>

	<!-- Meta properties for embed -->
	<meta property="og:title" content="silicone-server.xyz">
	<meta property="og:description" content="A little Mindustry server">
	<meta property="og:type" content="article">
	<meta property="og:url" content="https://silicone-server.xyz">
	<meta property="og:image" content="favicon.png">

	<!-- Twitter embeds -->
	<meta property="twitter:card" content="summary">
	<meta property="twitter:title" content="silicone-server.xyz">
	<meta property="twitter:description" content="A little Mindustry server">
	<meta property="twitter:image:src" content="./favicon.png">
</svelte:head>

<Header />

<main>
	<slot />
</main>

<Footer />

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	:global(body) {
		background-color: #111;
		color: #eee;
	}
	main {
		text-align: center;
		padding: 1em;
		margin: 40px auto;
		max-width: none;
		background-color: #222;
	}
	h1 {
		color: #ccc;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
	@media (min-width: 640px) {
		main {
			max-width: 50%;
		}
	}
</style>
