<script>
  export let message;
  export let data;
  console.log(message);
  console.log(data);

  let width = 0;
  let height = 0;
  let area = 0;

  let txt = ""

  $: {
    area = width + height;
    console.log(area);
  }
</script>

<!-- svelte applications -->

<div>
  <input type="number" bind:value={width} />
  <input type="number" bind:value={height} /> <br />
  <input type="text" bind:value={txt} />
  <button on:click={() => console.log(txt)}>log into console</button>
</div>

<main>
  <h1>{message}</h1>

  {#if txt === "fuck"}
    <h1>Fuckkkkkk</h1>
  {/if}
  {#each data as item}
    <div>
      <h1>{item.name}</h1>
    </div>
  {/each}
</main>
