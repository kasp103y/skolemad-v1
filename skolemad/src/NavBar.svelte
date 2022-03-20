<script>
  import Router, { location, link } from "svelte-spa-router";
  import Bestil from "./pages/Bestil.svelte";
  import Home from "./pages/Home.svelte";
  import Konto from "./pages/Konto.svelte";
  import LogIndPage from "./pages/LogIndPage.svelte";
</script>

<nav>
  <a href="/">Home</a>
  <a href="/#/bestil">Bestil</a>
  <a href="/#/konto">Konto</a>
  <a href="/#/logInd">Log Ind</a>
</nav>

<Router
  routes={{
    "/": Home,
    "/bestil": Bestil,
    "/konto": Konto,
    "/logInd": LogIndPage,
  }}
/>
