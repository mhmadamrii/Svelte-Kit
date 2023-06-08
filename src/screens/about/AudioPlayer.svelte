<script context="module">
  const players = new Set();

  export function stopAll() {
    players.forEach((p) => p.pause());
  }
</script>

<script>
  import { onMount } from "svelte";

  export let src;

  let player;

  onMount(() => {
    // Like players.push(player)
    players.add(player);
    player.play();
  });
</script>

<div style="border: 1px solid red">
  <audio bind:this={player} {src} style="border: 1px solid red" controls>
    <track kind="captions" />
  </audio>
</div>
