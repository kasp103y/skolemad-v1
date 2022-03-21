<script>
  import Button from "./Button.svelte";
</script>

<section class="wrapper">
  <section class="video-hero">
    <video autoplay muted loop id="myVideo">
      <source src="hero-video.mp4" type="video/mp4" />
    </video>
  </section>

  <section class="hero">
    <div>
      <h1>SkoleMad</h1>
      <p class="p-lead">Vi står for madpakken, så står du får resten.</p>
      <div class="knapper">
        <Button>Log ind</Button><Button>Opret Bruger</Button>
      </div>
    </div>
  </section>
  <div class="arrow" />
</section>

<style>
  .arrow {
    border-left: var(--spacing-1) solid var(--background);
    border-top: var(--spacing-1) solid var(--background);
    transform: rotate(225deg);
    height: 2rem;
    width: 2rem;
    grid-area: 1/1;
    justify-self: center;
    align-self: end;
    margin-bottom: 10vh;
    mix-blend-mode: difference;
    animation-name: bounce;
    animation-duration: 2s;
    animation-iteration-count: infinite;
    animation-direction: alternate;
  }

  @keyframes bounce {
    0% {
      transform: translateY(0) rotate(225deg);
    }
    20%,
    50%,
    80%,
    100% {
      transform: translateY(0) rotate(225deg);
    }
    40% {
      transform: translateY(-15px) rotate(225deg);
    }

    60% {
      transform: translateY(-10px) rotate(225deg);
    }
  }

  .wrapper {
    display: grid;
    overflow: hidden;
  }

  .video-hero,
  .hero {
    grid-area: 1/1;
  }
  video {
    min-height: 90vh;
    width: 100vw;
    position: relative;
    z-index: -10;
    mix-blend-mode: multiply;
    overflow: hidden;
    aspect-ratio: 16/9;
  }
  .knapper {
    display: flex;
    justify-content: start;
    gap: var(--spacing-4);
  }

  .hero {
    /*  background-image: url("../barn-mad-1.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    min-height: 90vh;
    background-position: 58% 37%; */
    display: grid;
    justify-content: start;
    align-content: center;
    padding-left: var(--spacing-16);
  }

  .hero > * {
    margin-top: var(--spacing-2);
    color: var(--background);
  }
  /*  h1,
  p {
    text-align: center;
  } */
  div {
    max-width: 30rem;
  }
</style>
