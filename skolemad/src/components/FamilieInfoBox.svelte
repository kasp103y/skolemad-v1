<script>
  import Button from "./Button.svelte";
</script>

<div class="box">
  <p class="header">Familie Nitten</p>
  <div>
    <p class="value">Skole:</p>
    <p>Kalvebod Fælled Skole</p>
  </div>
  <p class="value">Børn:</p>
  <p class="kids_value">Bigitte Nitten - 8år - 3.X</p>
  <p>Bitten Nitten - 15år - 9.Ø</p>
</div>

<style>
  .box {
    background-color: var(--white);
    border: var(--primary) var(--border-width-primary) solid;
    border-radius: var(--border-rounded);
    padding: var(--spacing-4);
    height: fit-content;
  }
  .kids_value {
    padding-bottom: var(--spacing-2);
  }
  .value {
    font-weight: bolder;
    font-style: italic;
  }
  p {
    margin: 0;
    font-size: var(--paragraf-m);
  }
  .header {
    font-size: var(--heading-three-m);
    font-weight: bolder;
    text-decoration: underline;
  }
  p + p {
    padding-block: var(--spacing-1);
    padding-right: var(--spacing-8);
  }
  div {
    padding-block: var(--spacing-2);
  }
</style>
