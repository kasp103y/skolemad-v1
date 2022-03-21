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
      <div class="arrow" />
    </div>
  </section>
</section>

<style>
  .video-hero {
    display: none;
  }

  .wrapper {
    display: grid;
    overflow: hidden;
  }

  .knapper {
    display: flex;
    justify-content: center;
    gap: var(--spacing-4);
  }

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
    color: var(--background);
  }
  h1,
  p {
    text-align: center;
  }
  div {
    max-width: 30rem;
  }

  .arrow {
    display: none;
  }

  @media screen and (min-width: 800px) {
    .knapper {
      justify-content: start;
    }
    h1,
    p {
      text-align: left;
    }
    .hero {
      background-image: none;
      display: grid;
      justify-content: start;
      align-content: center;
      padding-left: var(--spacing-16);
    }

    .video-hero,
    .hero {
      grid-area: 1/1;
    }

    .video-hero {
      display: block;
      background-color: darkgray;
      z-index: -20;
    }
    video {
      max-height: 90vh;
      width: 100vw;
      position: relative;
      z-index: -10;
      mix-blend-mode: multiply;
      overflow: hidden;
      aspect-ratio: 16/9;
      object-fit: cover;
      display: block;
    }

    .arrow {
      display: block;
      border-left: 5px solid var(--background);
      border-top: 5px solid var(--background);
      transform: rotate(225deg);
      height: 1.5rem;
      width: 1.5rem;
      grid-area: 1/1;
      justify-self: center;
      align-self: end;
      margin: var(--spacing-4);
      z-index: -1;

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
  }
</style>
