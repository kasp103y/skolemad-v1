<script>
  import { slide } from "svelte/transition";
  export let entry;
  import Button from "./Button.svelte";
  let isOpen = false;
  const toggle = () => (isOpen = !isOpen);
</script>

<div>
  <button on:click={toggle} aria-expanded={isOpen}
    ><svg
      style="tran"
      width="20"
      height="20"
      fill="none"
      stroke-linecap="round"
      stroke-linejoin="round"
      stroke-width="2"
      viewBox="0 0 24 24"
      stroke="currentColor"><path d="M9 5l7 7-7 7" /></svg
    >
    {entry[0]}
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

  button {
    border: none;
    background: var(--font);
    color: var(--background);
    display: block;
    border-radius: var(--border-rounded);
    font-size: 36px;
    cursor: pointer;

    padding: var(--spacing-1) var(--spacing-2);

    min-width: 30rem;
  }

  ul {
    background-color: var(--accent);
    color: var(--background);
    padding: var(--spacing-4);
    margin: -1rem 0;
    border-radius: var(--border-rounded);
    z-index: -10;
    position: relative;
  }

  svg {
    transition: transform 0.2s ease-in;
  }

  [aria-expanded="true"] svg {
    transform: rotate(0.25turn);
  }
</style>
