<script>
  import Router, { location, link } from "svelte-spa-router";
  import Bestil from "./pages/Bestil.svelte";
  import Home from "./pages/Home.svelte";
  import Konto from "./pages/Konto.svelte";
  import LogIndPage from "./pages/LogIndPage.svelte";
  import OpretBrugerPage from "./pages/OpretBrugerPage.svelte";
  import GlemtKodeOrd from "./pages/GlemtKodeOrd.svelte";
</script>

<header>
  <nav>
    <div>
      <a class="logo-link" href="/">
        <p class="logo">Skole<span>Mad</span></p>
      </a>
    </div>

    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="/#/bestil">Bestil</a></li>
      <li><a href="/#/konto">Konto</a></li>
      <li><a href="/#/logInd">Log Ind</a></li>

      <li class="hidden"><a href="/#/opret">OPret</a></li>
      <li class="hidden"><a href="/#/glemt">glemt</a></li>
    </ul>
  </nav>

  <Router
    routes={{
      "/": Home,
      "/bestil": Bestil,
      "/konto": Konto,
      "/logInd": LogIndPage,
      "/opret": OpretBrugerPage,
      "/glemt": GlemtKodeOrd,
    }}
  />
</header>

<style>
  .hidden {
    display: none;
  }
  /*   ul {
    background-color: var(--primary);
    width: 100vw;
    height: 100vh;
    position: absolute;
    top: 0%;
    left: -100%;
  } */

  /*  .bar {
    width: 2rem;
    border-radius: var(--border-rounded);
    height: 0.3rem;
    margin-bottom: 0.2rem;
    background-color: var(--background);
  }

  .open {
    top: 0%;
    left: 100%;
  } */

  .logo-link {
    display: flex;
    align-content: center;
  }

  .logo {
    font-size: var(--heading-five);
  }

  a {
    text-decoration: none;
    color: var(--font);
    color: var(--background);
    font-weight: 700;

    transition: ease 250ms;
  }

  nav {
    background-color: var(--primary-nav);

    width: 100vw;
    position: fixed;
    z-index: 1000000000;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  ul {
    background-color: none;
    width: auto;
    height: auto;
    position: static;
    display: flex;
    justify-content: center;
    padding: 0;
  }

  span {
    color: var(--font);
  }

  div {
    align-self: center;
  }

  nav ul {
    gap: var(--spacing-4);
    list-style: none;
    display: flex;
  }

  li {
    align-self: center;
  }

  a:hover {
    color: var(--font);
  }

  @media screen and (min-width: 800px) {
    /*   .burger {
      display: none;
    } */
    nav {
      background-color: var(--primary-nav);
      height: 3vh;
      width: 100vw;
      position: fixed;
      z-index: 1000000000;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      padding: var(--spacing-4);
    }

    ul {
      background-color: none;
      width: auto;
      height: auto;
      position: static;
    }

    span {
      color: var(--font);
    }

    div {
      align-self: center;
    }

    nav ul {
      gap: var(--spacing-4);
      list-style: none;
      display: flex;
    }

    li {
      align-self: center;
    }

    a:hover {
      color: var(--font);
    }
  }
</style>
