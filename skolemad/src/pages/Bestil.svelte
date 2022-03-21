<script>
  import MenuValg from "../components/MenuValg.svelte";
  import MyAccordion from "../components/MyAccordion.svelte";
  import Menu from "../components/Menu.svelte";
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
        <MenuValg>Normal menu</MenuValg>
        <MenuValg>Vegetar menu</MenuValg>
        <MenuValg>Halal menu</MenuValg>
      </section>
    </section>
  </section>
  <div class="section right-content"><aside><Menu /></aside></div>
</main>

<style>
  .bestil-menu {
    display: flex;
  }
</style>
