<!-- persist the navigation to the currently set in the store -->
<script>
	// FIXME: add type checking
	// @ts-nocheck

	import { activeLink } from '../store/store.js';
	// import ArrowUpRight from '../public/arrow-up-right.svg';
	import ArrowUpRight from '../public/MaterialSymbolsArrowOutward.svelte';

	let currentActiveLink = '';

	activeLink.subscribe((value) => {
		currentActiveLink = value;
	});

	const updateActiveLink = (
		/** @type {{ target: { getAttribute: (arg0: string) => string; }; }} */ event
	) => {
		currentActiveLink = event.target.getAttribute('href');
		activeLink.set(currentActiveLink);
		//   console.log();
	};
</script>

<nav>
	<a
		class="nav-link {currentActiveLink === '/' ? 'active-link' : ''}"
		href="/"
		on:click={updateActiveLink}>Home</a
	>
	<a
		class="nav-link {currentActiveLink === '/art' ? 'active-link' : ''}"
		href="/art"
		on:click={updateActiveLink}>Art</a
	>
	<a
		class="nav-link {currentActiveLink === '/about' ? 'active-link' : ''}"
		href="/about"
		on:click={updateActiveLink}>About</a
	>
</nav>

<style>
	.nav-link {
		font-family: Arial, Helvetica, sans-serif;
		text-decoration: none;
		font-size: 16px;
		margin-right: 8px;
	}

	a:hover {
		text-decoration: underline;
	}

	.active-link {
		text-decoration: underline;
	}
</style>
