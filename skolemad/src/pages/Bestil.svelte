<script>
  import MenuValg from "../components/MenuValg.svelte";
  import MyAccordion from "../components/MyAccordion.svelte";
  import Button from "../components/Button.svelte";
  import Menu from "../components/Menu.svelte";
  import KontoInfoBox from "../components/KontoInfoBox.svelte";
  const data = {
    "Vælg barn": ["Nitten Bittensen", "Bitten Bittensen"],
  };
</script>

<main>
  <section class="center-content">
    <section class="child-picker">
      <article>
        {#each Object.entries(data) as entry}
          <MyAccordion {entry} />
        {/each}
      </article>
    </section>
    <section class="bestil-menu">
      <section class="menu">
        <MenuValg>Normal menu - 300 kr</MenuValg>
        <MenuValg>Vegetar menu - 300 kr</MenuValg>
        <MenuValg>Halal menu - 300 kr</MenuValg>
      </section>
      <section class="knapper">
        <Button>Bestil</Button>
      </section>
      <section class="Konto">
        <KontoInfoBox />
      </section>
    </section>
  </section>
  <div class="right-content"><aside><Menu /></aside></div>
</main>

<style>
  .knapper {
    margin-top: var(--spacing-4);
  }
</style>
