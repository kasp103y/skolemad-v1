<script>
  import Button from "./Button.svelte";
</script>

<div class="box">
  <p>Konto</p>
  <p>Rådighedsbeløb</p>
  <div>
    <div class="penge_value">700kr.</div>
    <Button>Indsæt penge</Button>
  </div>
  <p>Lav fast overførsel med</p>
  <Button>Betalingsservice</Button>
</div>

<style>
  .box {
    margin: 5rem;
    background-color: var(--white);
    border: var(--primary) var(--border-width-primary) solid;
    border-radius: var(--border-rounded);
    padding: var(--spacing-2);
    width: var(--spacing-36);
  }
</style>
