<script lang="ts">
	// import Header from '$lib/header/Header.svelte';
	import Footer from "./components/Footer.svelte";
	import '../app.css';
</script>

<!-- <Header /> -->

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
