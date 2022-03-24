<script>
  import MenuValg from "../components/MenuValg.svelte";
  import MyAccordion from "../components/MyAccordion.svelte";
  import Button from "../components/Button.svelte";
  import Menu from "../components/Menu.svelte";
  import KontoInfoBox from "../components/KontoInfoBox.svelte";

  const data = {
    "Vælg barn": [
      "Nitten Bittensen",
      "Bitten Bittensen",
      "Bestil for alle børn",
    ],
  };
  const dataTo = {
    Marts: [
      "Jan",
      "Feb",
      "Mar",
      "Apr",
      "Maj",
      "Jun",
      "Jul",
      "Aug",
      "Sep",
      "Now",
      "Dec",
    ],
  };
</script>

<main>
  <section class="center-content">
    <section class="wrapper">
      <section class="child-picker">
        <article>
          {#each Object.entries(data) as entry}
            <MyAccordion {entry} />
          {/each}
        </article>
      </section>
      '
      <article class="header">
        <h3>Bestil for</h3>
        <article>
          {#each Object.entries(dataTo) as entry}
            <MyAccordion type="month" {entry} />
          {/each}
        </article>
        <h3>måned</h3>
      </article>

      <section class="bestil-menu">
        <section>
          <section class="menu">
            <MenuValg>Normal menu - 300 kr</MenuValg>
            <MenuValg>Vegetar menu - 300 kr</MenuValg>
            <MenuValg>Halal menu - 300 kr</MenuValg>
          </section>
          <section class="knapper">
            <Button>Bestil</Button>
          </section>
          <section class="knapper">
            <p>Lav fast månedlig bestilling</p>
            <Button type="accent">Fast bestilling</Button>
          </section>
        </section>
        <section class="konto">
          <KontoInfoBox />
        </section>
      </section>
    </section>
  </section>
  <div class="right-content"><aside><Menu /></aside></div>
</main>

<style>
  .header {
    display: flex;
    align-content: center;
  }
  .knapper {
    margin-top: var(--spacing-4);
  }
  .wrapper {
    padding-top: var(--spacing-16);
  }

  .child-picker {
    display: flex;
    gap: var(--spacing-4);
  }
  @media screen and (min-width: 800px) {
    .wrapper {
      padding-top: var(--spacing-4);
    }

    .konto {
      margin-left: var(--spacing-8);
    }
  }
  .bestil-menu {
    display: flex;
    flex-flow: wrap;
  }
</style>
