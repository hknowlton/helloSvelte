<script>
  export let name;
  const src = "https://avatars2.githubusercontent.com/u/23346903?s=460&v=4";
  import AboutMe from "./AboutMe.svelte";
  import Count from "./Count.svelte";
  import Cats from "./Cats.svelte";
</script>

<style>
  .marquee {
    position: relative;
  }

  .marquee div {
    width: 200%;
    position: absolute;
    animation: marquee 5s linear infinite;
    font-weight: 100;
  }

  @keyframes marquee {
    0% {
      left: 20%;
    }
    100% {
      left: -130%;
    }
  }
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  img {
    max-height: 100px;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <h1>Hello {name}!</h1>
  <img {src} alt="photo" />
  <div class="marquee">
    <div>
      <p>
        This is my first
        <b>Svelte</b>
        app, and it is pretty neat.
      </p>
    </div>
  </div>
  <AboutMe />
  <Count />
  <Cats />
</main>
