<script context="module" lang="ts">
	export async function load({params, fetch}: {params: any, fetch: any}) {
		try {
			const id = params.id;
			const res = await fetch(`http://jsonplaceholder.typicode.com/posts/${id}`);
			const json = await res.json();
			return {
				props: {
					post: json,
				}
			}
		} catch (err) {
			console.error(err)
		}
	}
</script>

<script lang="ts">
export let post: any;
</script>

<main>
	<h1>{post.title}</h1>
	<p>{post.body}</p>
</main>

<style>
	@media (min-width: 640px) {
		.posts {
			grid-template-columns: 1fr 1fr;
		}
	}
</style>