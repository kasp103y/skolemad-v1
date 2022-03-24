<script>
  import { slide } from "svelte/transition";
  export let entry;
  export let type;

  let isOpen = false;
  const toggle = () => (isOpen = !isOpen);
</script>

<div class={type}>
  <button on:click={toggle} aria-expanded={isOpen}>
    {entry[0]}<svg
      style="tran"
      width="20"
      height="20"
      fill="none"
      stroke-linecap="round"
      stroke-linejoin="round"
      stroke-width="6"
      viewBox="0 0 24 24"
      stroke="currentColor"><path d="M9 5l7 7-7 7" /></svg
    >
  </button>
  {#if isOpen}
    <ul transition:slide={{ duration: 300 }}>
      {#each entry[1] as item}
        <li>{item}</li>
      {/each}
    </ul>
  {/if}
</div>

<style>
  div {
    margin-bottom: var(--spacing-4);
  }

  ul {
    max-width: 40rem;
  }

  .month button {
    border: none;
    background: var(--knapper);
    color: var(--font);
    display: flex;
    border-radius: var(--border-rounded);
    font-size: var(--font-size-lg);
    cursor: pointer;
    justify-content: center;
    align-content: center;
    min-width: 10rem;
    margin: 0 var(--spacing-1);
    color: var(--background);

    padding: 0;
  }

  .month ul {
    color: var(--background);
    background-color: var(--knapper);
    padding: var(--spacing-4);
    margin: -1rem 0;
    border-radius: var(--border-rounded);
    z-index: -10;
    position: relative;

    list-style: none;
  }

  button {
    border: none;
    background: var(--font);
    color: var(--background);
    display: flex;
    border-radius: var(--border-rounded);
    font-size: var(--p-lead);
    cursor: pointer;
    justify-content: space-between;
    align-content: center;

    padding: var(--spacing-1) var(--spacing-2);

    min-width: 20rem;
  }

  svg {
    align-self: center;
  }

  ul {
    background-color: var(--accent);
    color: var(--background);
    padding: var(--spacing-4);
    margin: -1rem 0;
    border-radius: var(--border-rounded);
    z-index: -10;
    position: relative;
    list-style: none;
  }
  li {
    margin-top: var(--spacing-1);
  }

  svg {
    transition: transform 0.2s ease-in;
  }

  [aria-expanded="true"] svg {
    transform: rotate(0.25turn);
  }
</style>
