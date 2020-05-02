<script>
  import Home from "./pages/home.svelte";
  import Manga from "./components/Manga/manga.svelte";
  import Hentai from "./components/Hentai/hentai.svelte";
  import Anime from "./components/Anime/anime.svelte";
  import { Router, Link, Route } from "svelte-routing";
  //   import Home from "./routes/Home.svelte";
  //   import About from "./routes/About.svelte";
  //   import Blog from "./routes/Blog.svelte";
  export let url = "";
</script>

<style lang="scss" global>
  @import "./styles/global.scss";
</style>

<Router {url}>
  <!-- <nav class="header">
    <Link to="/">Home</Link>
    <Link to="anime">Anime</Link>
    <Link to="manga">Manga</Link>
    <Link to="hentai">Hentai</Link>
  </nav> -->

  <header class="header">
    <div class="container flex justify-between px-4">
      <div />
      <ol class="nav">
        <li>
          <Link to="/">Home</Link>
        </li>
        <li>
          <Link to="anime">Anime</Link>
        </li>
        <li>
          <Link to="manga">Manga</Link>
        </li>
        <li>
          <Link to="hentai">Hentai</Link>
        </li>
      </ol>
    </div>
  </header>
  <div>
    <!-- <Route path="blog/:id" component="{BlogPost}" /> -->
    <Route path="anime" component={Anime} />
    <Route path="manga" component={Manga} />
    <Route path="hentai" component={Hentai} />
    <Route path="/">
      <Home />
    </Route>
  </div>
</Router>
