<script>
    export let anime;
</script>

<div class="flex flex-wrap">
  {#each anime as info}
    <div class="w-1/5 p-1 flex-col justify-center">
      <div class="w-full flex-col relative">
        <img class="w-full" src={info.image_url} alt="info.title" />
        <div class="absolute rank">{info.rank || info.recommendation_count}</div>
      </div>
      <div class="">
        <p class="text-center">{info.title}</p>
      </div>

    </div>
  {:else}
    <p>Sorry I cannot load data from server</p>
  {/each}
</div>
