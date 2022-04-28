<script lang="ts">
	import Header from "../lib/components/Header.svelte";
	import Connect from "../lib/components/Connect.svelte";
	import Boxes from "../lib/components/Boxes.svelte";
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

<main>
	<Header/>
	<Connect/>
	<h1>silicone-server.xyz</h1>
	<p><strong>silicon-server.xyz: </strong>A little <a href="https://anuke.itch.io/mindustry">Mindustry</a> server</p><br>

	<Boxes />
</main>

<style>
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