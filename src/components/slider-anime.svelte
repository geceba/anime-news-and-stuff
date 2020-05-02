<script>
  import { onMount } from "svelte";
  let anime = [];

  onMount(async () => {
    const apiResponse = await fetch("https://api.jikan.moe/v3/top/anime");
    const animeJSON = await apiResponse.json();
    anime = animeJSON.top;
    console.log(anime);
  });
</script>

<div class="h-64 grid grid-rows-3 grid-flow-col gap-4">

  <div class="flex justify-center">
    <p>Anime Top</p>
  </div>

  <div class="flex flex-wrap">
    {#each anime as info}
      <div class="w-1/5 p-1">
        <img src={info.image_url} alt={info.title}>
        <p>{info.title}</p>
        <p>{info.rank}</p>
      </div>
    {:else}
      <p>Sorry I cannot load data from server</p>
    {/each}
  </div>
</div>
