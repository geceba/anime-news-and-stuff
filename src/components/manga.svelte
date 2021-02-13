<script>
  import Card from './card.svelte';
  export let manga;
</script>

<div class="h-64 grid-flow-col gap-4">

  <div class="flex justify-center m-4">
    <p class="text-2xl font-bold">Anime Top</p>
  </div>

  <Card anime={manga}/>
  
</div>
