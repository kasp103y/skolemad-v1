<script>
  export let type = "default";
  export let mode = "default";
  function handleClick() {
    alert("Det du havde tænkt at gøre er gjort nu succesfyldt");
  }
</script>

<div>
  <button
    on:click={handleClick}
    class:inversed={mode === "inversed"}
    class={type}><slot /></button
  >
</div>

<style>
  /* div {
    display: flex;
    justify-content: center;
    margin-top: var(--spacing-4);
  } */
  button {
    color: var(--white);
    background-color: rgb(34, 199, 171);
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
    background: var(--primary);
  }

  button:hover {
    filter: brightness(0.7);
  }

  .secondary {
    background-color: transparent;
    border: var(--border-width-primary) solid rgb(34, 199, 171);

    color: rgb(34, 199, 171);
  }

  .accent {
    background-color: var(--accent);
    color: var(--background);
  }

  .danger {
    background-color: var(--btn-danger);
    color: var(--btn-danger-font);
  }

  .warning {
    background-color: var(--btn-warning);
    color: var(--font);
  }

  /*  .ghost {
    background-color: transparent;
    color: var(--secondary-font);
  }

  .white {
    background-color: var(--white);
    border: var(--primary) var(--border-width-primary) solid;
    border-radius: var(--border-rounded);
    color: black;
  }
  .link {
    background-color: transparent;
    color: var(--link-font-color);
  }

  .primary.inversed {
    background-color: var(--primary-font-color);
    color: var(--link-font-color);
  } */
</style>
