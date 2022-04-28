<script context="module" lang="ts">
	
    export async function load({fetch}: {fetch: any}) {
        try {
            const res = await fetch(`http://jsonplaceholder.typicode.com/posts/${page}`);
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
    <h1>Posts</h1>

    {JSON.stringify(post)}
</main>

<style>
	.posts {
		display: grid;
		grid-template-columns: 1fr;
		grid-gap: 2rem;
	}

	.post {
		border: 0.125rem solid white;
		padding: 10px;
		box-shadow: 0 0 15px #111;
	}

	.link {
		text-align: right;
		color: #5857b4;
	}

	.link a {
		text-align: right;
		color: #5857b4;
	}

	h2 {
		font-size: 1.5rem;
		font-weight: bold;
		margin: 0;
	}

	@media (min-width: 640px) {
		.posts {
			grid-template-columns: 1fr 1fr;
		}
	}
</style>