<script>
	import Router from 'svelte-spa-router';
	import routes from './routes.js';
</script>

<main>
	<Router {routes}/>
</main>

<style lang="scss" global>
 @import "./styles/global.scss";
</style>