<script>
  import Button from "./Button.svelte";
</script>

<section class="hero">
  <div>
    <h1>SkoleMad</h1>
    <p class="p-lead">
      SkoleMad tilbyder en nem og fleksibel frokostordning til dine børn
    </p>
    <Button>Log ind/Opret bruger</Button>
  </div>
</section>

<style>
  .hero {
    background-image: url("../barn-mad-1.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    min-height: 90vh;
    background-position: 58% 37%;
    display: grid;
    justify-content: center;
    align-content: center;
  }

  .hero > * {
    margin-top: var(--spacing-2);
  }

  div {
    max-width: 20rem;
  }
</style>
