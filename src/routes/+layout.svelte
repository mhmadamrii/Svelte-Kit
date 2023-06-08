<script>
  import "../app.css";
  import img from "$lib/tes.png";
</script>

<main>
  <div class="navbar bg-base-100">
    <div class="flex-1">
      <a class="btn btn-ghost normal-case text-xl">My World</a>
    </div>
    <div class="flex-none">
      <ul class="menu menu-horizontal px-1">
        <li><a>Interstellar</a></li>
        <li>
          <details>
            <summary> Options </summary>
            <ul class="p-2 bg-base-100">
              <li><a href="/">Home</a></li>
              <li><a href="/arna">My Love</a></li>
            </ul>
          </details>
        </li>
      </ul>
    </div>
  </div>
</main>

<slot />
