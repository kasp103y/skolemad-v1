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
  <p class="open_pop_2">Konto udtog</p>

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
  #pop_up_2 {
    z-index: 10;
    display: none;
    position: relative;
    top: -25rem;
    background-color: rgba(0, 0, 0, 0.452);
    height: 170vh;
    width: 174vh;
  }
  .pop_up_style_2 {
    background-color: var(--box-color);
    width: 36rem;
    padding: 2rem;
    margin-top: 2rem;
    position: absolute;
    top: 3rem;
    left: 28rem;
    border-radius: var(--border-rounded);
  }
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
  }
  .open_pop_2 {
    cursor: pointer;
    display: block;
    transition: ease 250ms;
    text-align: start;
    font-weight: 800;
    color: var(--background);
  }

  .open_pop_2:hover {
    color: var(--font);
  }
  .luk_knap_2 {
    cursor: pointer;
    font-weight: bolder;
    font-size: larger;
  }
  .luk_knap_2:hover {
    color: red;
  }

  .luk_knap_2 {
    height: 0;
    width: 0;
    background-color: none;
    border: none;
  }
</style>
