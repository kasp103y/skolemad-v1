<script>
  import Router, { location, link } from "svelte-spa-router";
  import Bestil from "../pages/Bestil.svelte";

  import FamilieInfoBox from "../components/FamilieInfoBox.svelte";
  import KontoInfobox from "../components/KontoInfoBox.svelte";
  import BestillingerValg from "../components/BestillingerValg.svelte";
  import BestilingOversigt from "../components/BestilingOversigt.svelte";
  import KontoUdtog from "../components/KontoUdtog.svelte";
</script>

<div class="flex_1">
  <FamilieInfoBox />
  <KontoInfobox />
</div>

<div class="flex_2">
  <div class="knapperX4">
    <BestillingerValg><a href="/#/bestil">Bestil mad</a></BestillingerValg>
    <BestillingerValg><a href="/#/bestil">Afbestilling</a></BestillingerValg>
    <BestilingOversigt />
    <KontoUdtog />
    <Router
      routes={{
        "/bestil": Bestil,
      }}
    />
  </div>
</div>

<style>
  .knapperX4 {
    margin: var(--spacing-8);
  }
  .flex_1 {
    padding-top: var(--spacing-8);
    display: flex;
    justify-content: space-between;
  }
  .flex_2 {
    display: flex;
    justify-content: space-between;
  }
  a {
    text-decoration: none;
  }
</style>
