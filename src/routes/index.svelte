<script lang="ts">
	import Header from "./components/Header.svelte";
	import Footer from "./components/Footer.svelte";
	import Connect from "./components/Connect.svelte";
	import Socials from "./components/Socials.svelte";
	import Boxes from "./components/Boxes.svelte";
</script>

<main>
	<Header/>
	<Connect/>
	<h1>silicone-server.xyz</h1>
	<p><strong>silicon-server.xyz: </strong>A little <a href="https://anuke.itch.io/mindustry">Mindustry</a> server</p><br>

	<Boxes />
	<Socials/>
	<Footer/>
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