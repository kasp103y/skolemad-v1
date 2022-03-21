<script>
  import Button from "./Button.svelte";
</script>

<div class="box">
  <p class="value">Konto</p>
  <p>Rådighedsbeløb</p>
  <div class="button_flex">
    <Button type="white">700kr.</Button>
    <Button>Indsæt penge</Button>
  </div>
  <div class="service_info">
    <p>Lav fast overførsel med</p>
    <div class="service_knap">
      <Button type="accent">Betalingsservice</Button>
    </div>
  </div>
</div>

<style>
  p {
    margin: 0;
  }
  .value {
    font-weight: bolder;
    font-style: italic;
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
    margin: 5rem;
    background-color: var(--box-color);

    border-radius: var(--border-rounded);
    padding: var(--spacing-2);
    /* width: var(--spacing-36); */
  }
</style>
