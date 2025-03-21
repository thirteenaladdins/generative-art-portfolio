<script lang="ts">
	import { activeLink } from '../store/store.js';
	import NavBar from '../components/NavBar.svelte';
	import '../app.css';
	import { onMount, getContext, tick } from 'svelte';
	// const { component, route } = getContext('routify');
	// update the current active link...?

	let currentActiveLink = '';
	let title = '';

	activeLink.subscribe((value) => {
		currentActiveLink = value;
		console.log(currentActiveLink);

		switch (currentActiveLink) {
			case '/':
				// title = 'momo';
				break;
			case '/art':
				// title = 'generative art';
				break;
			case '/about':
				// title = 'about';
				break;
			default:
				title = '404 Page Not Found';
		}
	});
</script>

<main class="container">
	<!-- render the header here depending on the page -->
	<h1>{title}</h1>
	<NavBar />
	<slot />
</main>
