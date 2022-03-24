<script>
  let active = false;
</script>

<button class:active on:click={() => (active = !active)}><slot /></button>

<style>
  button {
    height: 4rem;
    width: 20rem;
    padding: var(--spacing-2) var(--spacing-4);
    background-color: var(--background);
    border: var(--border-width-primary) solid var(--primary);
    margin-top: var(--spacing-2);
    border-radius: var(--border-rounded);
    font-weight: 800;
    cursor: pointer;
    display: block;
    transition: ease 250ms;
  }

  .active {
    background-color: var(--font);
    color: var(--background);
  }

  button:active {
    background-color: var(--font);
    color: var(--background);
    border: none;
  }

  button:hover {
    background-color: var(--font);
    color: var(--background);
  }
</style>
