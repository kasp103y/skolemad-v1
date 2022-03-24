<script></script>

<button> <slot /> </button>

<style>
  button {
    height: 4rem;
    width: 16rem;
    padding: var(--spacing-2) var(--spacing-4);
    background-color: var(--background);
    border: var(--border-width-seconday) solid var(--primary);
    margin-top: var(--spacing-2);
    border-radius: var(--border-rounded);
    cursor: pointer;
    display: block;
    transition: ease 250ms;
    text-align: start;
    font-weight: 800;
  }

  button:hover {
    background-color: var(--font);
    color: var(--background);
  }
</style>
