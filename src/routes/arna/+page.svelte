<script>
  import arna from "$lib/arna.jpg";
</script>

<main>
  <div class="hero min-h-screen" style="background-image: url('/src/lib/arnaaa.jpg');">
    <div class="hero-overlay bg-opacity-60" />
    <div class="hero-content text-center text-neutral-content">
      <div class="max-w-md">
        <button class="btn" onclick="my_modal_1.showModal()">open modal</button>
        <dialog id="my_modal_1" class="modal">
          <form method="dialog" class="modal-box">
            <h3 class="font-bold text-lg">Hello!</h3>
            <p class="py-4">Press ESC key or click the button below to close</p>
            <div class="modal-action">
              <!-- if there is a button in form, it will close the modal -->
              <button class="btn">Close</button>
            </div>
          </form>
        </dialog>
      </div>
    </div>
  </div>
</main>

<style>
</style>
