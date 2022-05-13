<script>
	import Router from 'svelte-spa-router';
	import Home from './pages/Home.svelte';
	import CompanyInfo from './pages/CompanyInfo.svelte';
	import Launch from './pages/Launch.svelte';
	import LaunchPads from './pages/LaunchPads.svelte';
	import Header from './components/Header.svelte';

	import NotFound from './pages/NotFound.svelte';

let routes = {
	"/": Home,
	"/company": CompanyInfo,
	"/launch": Launch,
	"/launch-pads": LaunchPads,
	"/*": NotFound

}

</script>

<Header />

<main>
	<Router {routes}/>
</main>

<style>
	
</style>