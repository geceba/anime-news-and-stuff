<script>
import {link} from 'svelte-spa-router';

</script>
<header class="header">
  <div class="container flex justify-between px-4">
    <div />
    <ol class="nav">
      <li>
        <a href="/" use:link>Animes</a>
      </li>
      <li>
        <a href="https://getwaves.io/" target="_blank">Mangas</a>
      </li>
      <li>
        <a href="/hentai" use:link>Hentai</a>
      </li>
    </ol>
  </div>
</header>
