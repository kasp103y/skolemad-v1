<script>
  export let type = "default";
  export let mode = "default";
</script>

<div>
  <button class:inversed={mode === "inversed"} class={type}><slot /></button>
</div>

<style>
  div {
    display: flex;
    justify-content: center;
    margin-top: var(--spacing-4);
  }
  button {
    color: var(--white);
    background-color: var(--primary);
    transition: 0.2s ease;
    padding: var(--spacing-2) var(--spacing-4);
    max-width: 15rem;

    text-transform: uppercase;
    border-radius: var(--border-rounded);
    border: none;
    font-weight: 800;
    cursor: pointer;
    display: inline-block;
  }

  .primary {
    background: var(--primary-color);
  }

  button:hover {
    filter: brightness(0.7);
  }

  .secondary {
    background-color: var(--secondary-color);
  }

  .accent {
    background-color: var(--accent-color);
  }

  .ghost {
    background-color: transparent;
    color: var(--secondary-font-color);
  }

  .link {
    background-color: transparent;
    color: var(--link-font-color);
  }

  .primary.inversed {
    background-color: var(--primary-font-color);
    color: var(--link-font-color);
  }
</style>
