<script>
  import Profile from "./Profile.svelte";

  let count = 0;
  let message = "Hello world";
</script>

<main>
  <Profile {count} {message} />
</main>
