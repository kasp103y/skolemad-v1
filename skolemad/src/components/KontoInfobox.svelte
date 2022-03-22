<script>
  import Button from "./Button.svelte";
  let amount = "500kr";
</script>

<div class="box">
  <h3>Konto</h3>
  <p class="amount">Rådighedsbeløb <span>{amount}</span></p>
  <div class="button_flex">
    <h4>Tilføj til konto</h4>
    <input type="number" />
    <Button type="submit">Indsæt penge</Button>
  </div>
  <div class="service_info">
    <p>Lav fast overførsel med</p>
    <div class="service_knap">
      <Button type="accent">Betalingsservice</Button>
    </div>
  </div>
</div>

<style>
  input {
    color: var(--font);

    transition: 0.2s ease;
    padding: var(--spacing-2) var(--spacing-4);
    max-width: 15rem;
    border: 3px solid green;
    text-transform: uppercase;
    border-radius: var(--border-rounded);
    border: none;
    font-weight: 800;
    cursor: pointer;
    display: inline-block;
  }

  span {
    font-weight: 900;
  }

  p {
    margin: 0;
    padding-bottom: var(--spacing-2);
  }
  .amount {
    text-decoration: underline;
  }
  .service_info {
    margin-top: var(--spacing-2);
  }
  .service_info p {
    padding-top: var(--spacing-2);
  }
  .service_knap {
    display: flex;
  }
  .button_flex {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    margin-top: var(--spacing-2);
  }
  /* .button_flex Button {
    padding-right: 2rem;
  } */
  .box {
    margin-left: var(--spacing-8);
    background-color: var(--box-color);

    border-radius: var(--border-rounded);
    padding: var(--spacing-4);
    width: 25rem;
  }
</style>
