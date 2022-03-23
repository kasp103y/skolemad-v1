<script>
  import MenuValg from "../components/MenuValg.svelte";
  import MyAccordion from "../components/MyAccordion.svelte";
  import Button from "../components/Button.svelte";
  import Menu from "../components/Menu.svelte";
  import KontoInfoBox from "../components/KontoInfoBox.svelte";
  const data = {
    "Vælg barn": ["Nitten Bittensen", "Bitten Bittensen"],
  };
  const dataTo = {
    "Vælg måned": [
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

  let month = "Marts";
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
        <article>
          {#each Object.entries(dataTo) as entry}
            <MyAccordion {entry} />
          {/each}
        </article>
      </section>
      <h2>Bestil for {month} måned</h2>
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
