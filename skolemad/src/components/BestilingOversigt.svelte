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
      <p>Forløbigt Kontoudtog famile Nitten</p>
      <div class="flex">
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
        <tr>
          <th>Dato</th>
          <th>Betalingsform</th>
          <th>Beløb <br /> kr</th>
          <th>Saldo <br />kr</th>
        </tr>
        <tr>
          <td>10/1-22 </td>
          <td> Indbetalt - Mobilepay</td>
          <td>408.00</td>
          <td>408.00</td>
        </tr>
        <tr>
          <td>28/2-21 (bestilt 26/1-21)</td>
          <td>Begitte - Køb februar</td>
          <td>-230.00</td>
          <td>178.00</td>
        </tr>

        <tr>
          <td>14/3-21</td>
          <td> Indbetalt - Dankort</td>
          <td>900.00</td>
          <td>1078.00</td>
        </tr>
        <tr>
          <td>5/4-21 (bestilt 14/3-21)</td>
          <td>Begitte - Køb April</td>
          <td>-414.00</td>
          <td>664.00</td>
        </tr>
        <tr>
          <td>5/4-21 (bestilt 14/3-21)</td>
          <td>Bitten - Køb April</td>
          <td>-414.00</td>
          <td>250.00</td>
        </tr>

        <tr>
          <td>21/4-21</td>
          <td> Indbetalt - Dankort</td>
          <td>800.00</td>
          <td>1050.00</td>
        </tr>
        <tr>
          <td>1/5-21 (bestilt 25/5-21)</td>
          <td>Bitten - Køb Maj</td>
          <td>-299.00</td>
          <td>751.00</td>
        </tr>
        <tr>
          <td>1/5-21 (bestilt 25/5-21)</td>
          <td>Begitte - Køb Maj</td>
          <td>-299.00</td>
          <td>452.00</td>
        </tr>
      </table>
    </div>
  </div>
</div>

<style>
  td {
    padding: 0.5rem;
  }
  p {
    text-align: center;
  }
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
    background-color: var(--box-color);
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
  .form {
    margin-block: 0;
  }
  input {
    width: 3rem;
    height: 1.5rem;
  }
  table,
  th,
  td {
    border: 1px solid var(--primary);
  }
  .flex {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
  }
</style>
