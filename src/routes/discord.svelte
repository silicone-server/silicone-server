<script context="module">
	let url = "https://discord.gg/aBTkpvdZAU";

	export async function load() {
		return {
			status: 302,
			redirect: url
		}
	}
</script>

<svelte:head>
	<title>discord</title>
	<meta name="description" content="Discord redirect" />
</svelte:head>

<div class="content">
	<h1>you are being redirected to our <a href={url}>discord</a></h1>
</div>