<script>
  window.addEventListener("DOMContentLoaded", start);

  function start() {
    console.log("start_2");

    document.querySelector(".luk_knap_2").addEventListener("click", lukPopup2);
    document
      .querySelector(".open_pop_2")
      .addEventListener("click", clickOpenPopupHandler2);
  }

  function lukPopup2() {
    console.log("lukPopup_2");
    document.querySelector("#pop_up_2").style.display = "none";
  }

  function clickOpenPopupHandler2() {
    console.log("virker det?_2");
    document.querySelector("#pop_up_2").style.display = "block";
  }
</script>

<div class="flex">
  <button class="open_pop_2"> Konto udtog </button>

  <div id="pop_up_2">
    <div class="pop_up_style_2">
      <button class="luk_knap_2">X</button>
      <h3>Dette er en POP TEST_2</h3>
    </div>
  </div>
</div>

<style>
  .flex {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
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
  .pop_up_style_2 {
    border: solid 5px black;
    width: fit-content;
    padding: 2rem;
    margin-top: 2rem;
  }
  #pop_up_2 {
    display: none;
    position: absolute;
    top: 37rem;
    left: 45rem;
  }
</style>
