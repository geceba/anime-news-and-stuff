<script>
  import { onMount } from "svelte";
  import Manga from "./../components/manga.svelte";

  let manga = [];

  const urlApi = "https://api.jikan.moe/v3/manga/1/recommendations";

  onMount(async () => {
    const resp = await fetch(`${urlApi}`);
	const { recommendations } = await resp.json();
    manga = recommendations;
  });
</script>

<Manga {manga} />
