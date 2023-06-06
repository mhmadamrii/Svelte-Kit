<script>
  let sayHello = "Hello world";
  let isAlert = false;
  let inputValue = "";

  function handleChange(event) {
    inputValue = event.target.value;
    console.log("input value", inputValue);
  }

  function showAlert() {
    isAlert = true;
  }
</script>

<main>
  <center>
    <h1>{sayHello}</h1>
    <button class="btn" on:click={showAlert} on:input={handleChange}>Submit</button>
    <input type="text" placeholder="Type here" class="input input-bordered input-success w-full max-w-xs" bind:value={inputValue} />

    {#if isAlert}
      <div class="alert alert-success">
        <svg xmlns="http://www.w3.org/2000/svg" class="stroke-current shrink-0 h-6 w-6" fill="none" viewBox="0 0 24 24"
          ><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg
        >
        <span>Your purchase has been confirmed!</span>
      </div>
      <h1>{inputValue}</h1>
    {/if}

    <!-- Open the modal using ID.showModal() method -->
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
  </center>
</main>
