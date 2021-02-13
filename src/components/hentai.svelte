<script>
  import { onMount } from "svelte";
  import Card from './card.svelte';
  let hentai = [];

  onMount(async () => {
    const apiResponse = await fetch("https://api.jikan.moe/v3/search/anime?rated=rx");
    const animeJSON = await apiResponse.json();
    hentai = animeJSON.results;
  });
</script>

<div class="h-64 grid-flow-col gap-4">

  <div class="flex justify-center m-4">
    <p class="text-2xl font-bold">Anime Top</p>
  </div>

  <Card anime={hentai}/>
  
</div>
