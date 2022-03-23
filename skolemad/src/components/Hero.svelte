<script>
  import Button from "./Button.svelte";
  import Proof from "./Proof.svelte";
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
      <p class="p-lead">
        Vi står for madpakken, så står du for det der virkelig tæller.
      </p>
      <div class="knapper">
        <Button>Log ind</Button><Button type="secondary">Opret Bruger</Button>
      </div>
      <div class="arrow" />
    </div>
  </section>
  <section class="proof">
    <p class="p-lead-white">SkoleMad bruges af:</p>
    <article class="proofs">
      <Proof>396 instutitioner</Proof>
      <Proof>51 køkkener</Proof>
      <Proof>141.731 brugere</Proof>
    </article>
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
    background-image: url("../hero-video_Moment.jpg");
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

  .proof {
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

    .proof {
      display: block;
      grid-area: 1/1;
      justify-self: center;
      align-self: end;
      margin: var(--spacing-4) 0;
    }

    .proofs {
      display: flex;
      gap: var(--spacing-4);
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

    .proof {
      grid-area: 1/1;
      justify-self: center;
      align-self: end;
      margin: var(--spacing-4) 0;
    }

    .proofs {
      display: flex;
      gap: var(--spacing-4);
    }

    .video-hero {
      display: block;
      background-color: #a8a8a8;
      z-index: -20;
    }
    video {
      position: relative;
      height: 90vh;
      width: 100%;
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
