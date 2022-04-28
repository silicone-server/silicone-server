<script context="module" lang="ts">
	export async function load({params, fetch}: {params: any, fetch: any}) {
		try {
			const id = params.id;
			const res = await fetch(`https://raw.githubusercontent.com/silicone-server/dgc/main/blog.json`);
            const json = await res.json();

			console.log();
			console.log();
			console.log();

            return {
                props: {
                    title: json["posts"][id - 1]["title"],
					body: json["posts"][id - 1]["body"],
					id: json["posts"][id - 1]["id"],
                }
            }
		} catch (err) {
			console.error(err)
		}
	}
</script>

<script lang="ts">
export let title: any;
export let body: any;
export let id: any;
</script>

<main>
	<h1>{title} [#{id}]</h1>
	<p><span style="white-space: pre-line">{body}</span></p>
</main>

<style>
</style>