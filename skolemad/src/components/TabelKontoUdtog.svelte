<script></script>

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
    <td> Primo</td>
    <td>234.00</td>
    <td>234.00</td>
  </tr>
  <tr>
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

<style>
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
