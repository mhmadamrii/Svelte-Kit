<script>
  import { onMount } from "svelte"
  let posts = []

  async function fetchPosts() {
    const res = await fetch("https://jsonplaceholder.typicode.com/posts")
    console.log(res)
    posts = await res.json()
  }

  onMount(() => {
    fetchPosts()
  })
</script>

<main>
  <center>
    <h1>The posts may you like..</h1>
    {#each posts as post }
      <h1>{post.title}</h1>
    {/each}
  </center>
</main>