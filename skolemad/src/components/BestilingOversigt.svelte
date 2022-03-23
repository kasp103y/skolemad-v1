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
        <tr class="head_info">
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
        <tr class="farve">
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
        <tr class="farve">
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

        <tr class="farve">
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
        <tr class="farve">
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
  #pop_up {
    display: none;
    position: relative;
    top: -33.7rem;
    background-color: rgba(0, 0, 0, 0.452);
    height: 155vh;
    width: 174vh;
  }
  .pop_up_style {
    background-color: var(--box-color);
    width: 36rem;
    padding: 2rem;
    margin-top: 2rem;
    position: absolute;
    top: 3rem;
    left: 28rem;
  }
  .head_info {
    background-color: silver;
  }
  .farve {
    background-color: ghostwhite;
  }
  input {
    color: var(--font);

    transition: 0.2s ease;
    max-width: 15rem;
    border: 3px solid green;
    text-transform: uppercase;
    border-radius: var(--border-rounded);
    border: none;
    font-weight: 800;
    cursor: pointer;
    display: inline-block;
  }
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
    padding-block: var(--spacing-2);
  }
  .luk_knap {
    height: 0;
    width: 0;
    background-color: none;
    border: none;
  }
  .luk_knap {
    cursor: pointer;
    font-weight: bolder;
    font-size: larger;
  }
  .luk_knap:hover {
    color: red;
  }
  .open_pop {
    height: 4rem;
    width: 12rem;
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

  .open_pop:hover {
    background-color: var(--font);
    color: var(--background);
  }

  .form {
    margin-block: 0;
  }
  input {
    width: 3rem;
    height: 1.5rem;
  }

  .flex {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
  }
</style>
