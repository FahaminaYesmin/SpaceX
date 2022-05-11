<script>
	import Router from 'svelte-spa-router';
	import Home from './pages/Home.svelte';
	import CompanyInfo from './pages/CompanyInfo.svelte';
	import Launch from './pages/Launch.svelte';
	import LaunchPads from './pages/LaunchPads.svelte';
	import NotFound from './pages/NotFound.svelte';

let routes = {
	"/": Home,
	"/company": CompanyInfo,
	"/launch": Launch,
	"/launch-pads": LaunchPads

}

</script>

<!-- <nav>
	<a href="#/">Home</a>
	<a href="#/company">Company Information</a>
	<a href="#/launch">Launch</a>
	<a href="#/launch-pads">Launch Pads</a>
</nav> -->

<main>
	<Router {routes}/>
</main>

<style>
	
</style>