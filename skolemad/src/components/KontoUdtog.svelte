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
      <p>Forløbigt Kontoudtog famile Nitten</p>
      <div class="flex_1">
        <div>
          <label for="fname">Fra:</label>
          <input type="text" />
        </div>
        <div>
          <label for="fname">Til:</label>
          <input type="text" />
        </div>

        <p class="form">
          <label for="favoriteOnly">For:</label>
          <select name="favoriteOnly" id="favoriteOnly">
            <option>Bigitte</option>
            <option>Bitten</option>
            <option>Begge</option>
          </select>
        </p>
        <input type="submit" value="Hent" />
      </div>
      <p>10/1-22 - 1/4-22</p>
      <table>
        <tr class="head_info">
          <th>Dato</th>
          <th>Betalingsform</th>
          <th>Beløb <br /> kr</th>
          <th>Saldo <br />kr</th>
        </tr>
        <tr>
          <td>10/1-22 </td>
          <td> Primo</td>
          <td>234.00</td>
          <td>234.00</td>
        </tr>
        <tr class="farve">
          <td>11/3-22</td>
          <td>Mobilpay 6 23846: 6-1212345</td>
          <td>234.00</td>
          <td>234.00</td>
        </tr>
        <td>1/4-22</td>

        <td>Ultimo</td>
        <td>234.00</td>
        <td>234.00</td>
        <tr />
      </table>
    </div>
  </div>
</div>

<style>
  .head_info {
    background-color: silver;
  }
  .farve {
    background-color: ghostwhite;
  }
  td {
    padding: 0.5rem;
  }
  p {
    text-align: center;
  }
  .form {
    margin-block: 0;
  }
  input {
    width: 3rem;
    height: 1.5rem;
  }

  .flex_1 {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 20px;
    padding-block: var(--spacing-2);
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
    background-color: var(--box-color);
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
  .luk_knap_2 {
    height: 0;
    width: 0;
    background-color: none;
    border: none;
  }
</style>
