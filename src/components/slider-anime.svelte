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

<div class="h-64 grid-flow-col gap-4">

  <div class="flex justify-center m-4">
    <p class="text-2xl font-bold">Anime Top</p>
  </div>

  <div class="flex flex-wrap">
    {#each anime as info}
      <div class="w-1/5 p-1 flex-col justify-center">
        <div class="w-full flex-col relative">
            <img class="w-full" src={info.image_url} alt="info.title" />
            <div class="absolute rank">
                {info.rank}
            </div>
        </div>
        <div class="">
          <p class="text-center">{info.title}</p>
        </div>
        
      </div>
    {:else}
      <p>Sorry I cannot load data from server</p>
    {/each}
  </div>
</div>
