<script>
import SliderAnime from './../components/slider-anime.svelte';
let img = "assets/img/hori.svg";
</script>
<div class="banner">
  <div class="svg-group bg-gradient">
    <div class="svg-blob">
      <svg width="600" height="600" xmlns="http://www.w3.org/2000/svg">
        <linearGradient id="orangeToindianred">
          <stop stop-color="rgb(36, 31, 95)" offset="0%" />
          <stop stop-color="rgb(20, 20, 109)" offset="100%" />
        </linearGradient>
        <path
          fill="url(#orangeToindianred)"
          d="M418.8 127.8c30.3 30.6 46.6 71.9 59.9 113.9 13.4 42 23.9 84.8 14.4
          123.2-9.5 38.4-39 72.5-74.5 106-35.5 33.4-77.1 66.3-120.9 69.4-43.7
          3.1-89.8-23.6-113.6-60.8-23.7-37.3-25.2-85.2-44.1-130.5-18.8-45.3-54.9-87.9-59.5-134.6-4.5-46.7
          22.6-97.5 64.4-124.4 41.9-26.9 98.5-29.9 148.9-21.4 50.5 8.5 94.8 28.5
          125 59.2z" />
      </svg>
    </div>

    <div class="svg-wave svg-wave-bottom">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
        <linearGradient id="orangeToViolet">
          <stop stop-color="rgb(30, 40, 91)" offset="20%" />
          <stop stop-color="rgb(20, 20, 109)" offset="70%" />
          <stop  stop-color="rgb(36, 31, 85)" offset="100%" />
        </linearGradient>
        <path
          fill="url(#orangeToViolet)"
          fill-opacity="1"
          d="M0,96L48,85.3C96,75,192,53,288,58.7C384,64,480,96,576,128C672,160,768,192,864,197.3C960,203,1056,181,1152,149.3C1248,117,1344,75,1392,53.3L1440,32L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z" />
      </svg>
    </div>

    <header class="header">
      <div class="container flex justify-between px-4">
        <div />
        <ol class="nav">
          <li>
            <a href="https://www.blobmaker.app/" target="_blank">Animes</a>
          </li>
          <li>
            <a href="https://getwaves.io/" target="_blank">Mangas</a>
          </li>
          <li>
            <a href="https://undraw.co/illustrations" target="_blank">
              Hentai
            </a>
          </li>
        </ol>
      </div>
    </header>

    <div class="container h-full md:pb-40 pt-24 px-4 flex items-center">
      <div class="flex flex-wrap md:h-full items-center w-full">
        <div class="w-full md:w-1/2 md:pr-4 pb-16 md:pb-0">
          <h1 class="text-white font-bold text-4xl leading-snug">
            Anime news for weebs
            <br />
            What do you think?
            <br />
            Need information, you got it
          </h1>

          <p class="text-white md:mt-10 leading-loose">
            Explore and enjoy anime content
            <br />
            We want your money
          </p>
        </div>

        <div class="w-full md:w-1/2 flex">
          <div class="card">
            <img src="{img}" alt="waifu" style="height: 350px!important;">
          </div>
        </div>
      </div>
    </div>
  </div>

  <SliderAnime />
</div>
