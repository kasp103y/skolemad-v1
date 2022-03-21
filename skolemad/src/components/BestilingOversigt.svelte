<script>
  window.addEventListener("DOMContentLoaded", start);

  function start() {
    console.log("start");

    document.querySelector(".luk_knap").addEventListener("click", lukPopup);
    document
      .querySelector(".open_pop")
      .addEventListener("click", clickOpenPopupHandler);
  }

  function lukPopup() {
    console.log("lukPopup");
    document.querySelector("#pop_up").style.display = "none";
  }

  function clickOpenPopupHandler() {
    console.log("virker det?");
    document.querySelector("#pop_up").style.display = "block";
  }
</script>

<div class="flex">
  <button class="open_pop"> Bestillings oversigt </button>

  <div id="pop_up">
    <div class="pop_up_style">
      <button class="luk_knap">X</button>
      <h3>Dette er en POP TEST_1</h3>
    </div>
  </div>
</div>

<style>
  .flex {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .luk_knap {
    height: 0;
    width: 0;
    background-color: none;
    border: none;
  }
  .luk_knap button:hover {
    background-color: none;
  }
  button {
    height: 4rem;
    width: 20rem;
    padding: var(--spacing-2) var(--spacing-4);
    background-color: var(--background);
    border: var(--border-width-seconday) solid var(--primary);
    margin-top: var(--spacing-2);
    border-radius: var(--border-rounded);
    cursor: pointer;
    display: block;
    transition: ease 250ms;
    text-align: start;
    font-weight: 800;
  }

  button:hover {
    background-color: var(--font);
    color: var(--background);
  }
  .pop_up_style {
    border: solid 5px black;
    width: fit-content;
    padding: 2rem;
    margin-top: 2rem;
  }
  #pop_up {
    display: none;
    position: absolute;
    top: 37rem;
    left: 45rem;
  }
</style>
