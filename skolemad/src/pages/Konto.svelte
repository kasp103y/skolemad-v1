<script>
  import Router, { location, link } from "svelte-spa-router";
  import Bestil from "../pages/Bestil.svelte";
  import Button from "../components/Button.svelte";
  import FamilieInfoBox from "../components/FamilieInfoBox.svelte";
  import KontoInfobox from "../components/KontoInfoBox.svelte";
  import BestillingerValg from "../components/BestillingerValg.svelte";
  import BestilingOversigt from "../components/BestilingOversigt.svelte";
  import KontoUdtog from "../components/KontoUdtog.svelte";
</script>

<main>
  <section class="center-content">
    <div class="flex_1">
      <div>
        <FamilieInfoBox />
        <div class="bestil_mad">
          <Button><a href="/#/bestil">Bestil mad</a></Button>
        </div>
      </div>
      <KontoInfobox />
    </div>
  </section>
  <section class="funktioner">
    <div class="funktioner_knapper">
      <BestillingerValg><a href="/#/bestil">Afbestilling</a></BestillingerValg>
      <BestillingerValg>Afmeld Betalingsservice</BestillingerValg>
      <BestillingerValg>Skift kodeord</BestillingerValg>
      <BestillingerValg>Tilføj barn</BestillingerValg>

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
  .bestil_mad {
    padding-top: var(--spacing-8);
    text-align: center;
  }
  .center-content {
    grid-column: 2/4;
  }
  .funktioner {
    grid-column: 1;
    grid-row: 1;
    margin-top: var(--spacing-8);
    background-color: var(--accent);
  }

  .flex_1 {
    padding-top: var(--spacing-8);
    display: flex;
    justify-content: space-between;
    padding-inline: var(--spacing-16);
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
