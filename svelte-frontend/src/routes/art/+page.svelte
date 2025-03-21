<script>
	// import Jimp from 'jimp';
	import banshee from '../../images/banshee.png';

	let isExpanded = false;
	let thumbnailWidth = 300; // Smaller thumbnail size
	let thumbnailHeight = 300;

	let optimizedImage = '';
</script>

<main>
	<div class="content">
		<p class="title">banshee</p>

		<div class="image-container">
			<img
				src={banshee}
				alt="Banshee art"
				loading="lazy"
				decoding="async"
				width={thumbnailWidth}
				height={thumbnailHeight}
				class:expanded={isExpanded}
				on:click={() => (isExpanded = !isExpanded)}
			/>
			{#if isExpanded}
				<div class="overlay" on:click={() => (isExpanded = false)}>
					<button class="close-button" on:click={() => (isExpanded = false)}>×</button>
				</div>
			{/if}
		</div>
	</div>
</main>

<style>
	main {
		max-width: 800px;
		margin: 0 auto;
		padding: 2rem;
	}

	.content {
		margin-top: 4rem;
	}

	.title {
		font-family: Arial, Helvetica, sans-serif;
		color: #666;
		line-height: 1.6;
		margin-bottom: 2rem;
	}

	.image-container {
		position: relative;
		cursor: pointer;
	}

	img {
		max-width: 100%;
		height: auto;
		transition: all 0.3s ease;
	}

	img.expanded {
		position: fixed;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		max-width: 90vw;
		max-height: 90vh;
		z-index: 1000;
	}

	.overlay {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: rgba(0, 0, 0, 0.8);
		z-index: 999;
	}

	.close-button {
		position: fixed;
		top: 20px;
		right: 20px;
		background: none;
		border: none;
		color: white;
		font-size: 2rem;
		cursor: pointer;
		z-index: 1001;
		padding: 10px;
	}

	.close-button:hover {
		opacity: 0.8;
	}
</style>
