<script>
  import Router, { location, link } from "svelte-spa-router";
  import Bestil from "../pages/Bestil.svelte";

  import FamilieInfoBox from "../components/FamilieInfoBox.svelte";
  import KontoInfobox from "../components/KontoInfoBox.svelte";
  import BestillingerValg from "../components/BestillingerValg.svelte";
  import BestilingOversigt from "../components/BestilingOversigt.svelte";
  import KontoUdtog from "../components/KontoUdtog.svelte";
</script>

<main>
  <section class="center-content">
    <div class="flex_1">
      <FamilieInfoBox />
      <KontoInfobox />
    </div>
  </section>
  <section class="funktioner">
    <div class="funktioner_knapper">
      <BestillingerValg><a href="/#/bestil">Bestil mad</a></BestillingerValg>
      <BestillingerValg><a href="/#/bestil">Afbestilling</a></BestillingerValg>
      <BestillingerValg>Afmeld Betalingsservice</BestillingerValg>
      <BestillingerValg>Skift kodeord</BestillingerValg>
      <BestilingOversigt />
      <KontoUdtog />
      <Router
        routes={{
          "/bestil": Bestil,
        }}
      />
    </div>
  </section>
</main>

<style>
  .funktioner {
    grid-column: 1;
    grid-row: 1;
    margin-top: var(--spacing-16);
  }

  .flex_1 {
    padding-top: var(--spacing-8);
    display: flex;
    justify-content: space-between;
  }
  .funktioner_knapper {
    display: grid;
    justify-items: start;
    padding-left: var(--spacing-1);
    padding-top: 3rem;
  }
  a {
    text-decoration: none;
  }
</style>
