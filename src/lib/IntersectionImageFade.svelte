<script>

	import { onMount, onDestroy } from 'svelte';

	export let image1 = '';
	export let image2 = '';
	export let image3 = '';
	export let image4 = '';
	export let duration = 5000;
	export let title1 = '';
	export let title2 = '';
	export let note = '';

	let showFirstPair = true;
	let animationFrame;

	const animate = (timestamp, lastTime = 0, elapsed = 0) => {
		if (!lastTime) lastTime = timestamp;
		elapsed += timestamp - lastTime;
		
		if (elapsed >= duration) {
		showFirstPair = !showFirstPair;
		elapsed = 0;
		}
		
		animationFrame = requestAnimationFrame((t) => animate(t, timestamp, elapsed));
	};

	onMount(() => {
		animationFrame = requestAnimationFrame(animate);
		return () => cancelAnimationFrame(animationFrame);
	});

</script>


<div class="dual-fader-container">

	<div class="image-pair">
		{#if title1}<p class="pair-title">{title1}</p>{/if}
		<div class="image-wrapper">
		<img
			src={image1}
			alt={title1 + ' view A'}
			class="image"
			class:active={showFirstPair}
			style="transition-duration: {duration}ms"
		/>
		<img
			src={image2}
			alt={title1 + ' view B'}
			class="image"
			class:active={!showFirstPair}
			style="transition-duration: {duration}ms"
		/>
		</div>
	</div>

	<div class="image-pair">
		{#if title2}<p class="pair-title">{title2}</p>{/if}
		<div class="image-wrapper">
		<img
			src={image3}
			alt={title2 + ' view A'}
			class="image"
			class:active={showFirstPair}
			style="transition-duration: {duration}ms"
		/>
		<img
			src={image4}
			alt={title2 + ' view B'}
			class="image"
			class:active={!showFirstPair}
			style="transition-duration: {duration}ms"
		/>
		</div>
	</div>

</div>

<div class="note">
	<p>
		{note}
	</p>
</div>



<style>

	.dual-fader-container {
		display: flex;
		gap: 20px;
		justify-content: center;
		max-width: 100%;
		margin: 5px;
	}

	.image-pair {
		flex: 0 0 auto;
		width: clamp(150px, 40vw, 250px); 
	}

	.pair-title {
		font-size: 14px;
		font-family: OpenSansItalic;
		padding-left: 15px;
		margin-bottom: 0px;
		font-weight: normal;
		text-align: left;
		color: var(--brandGray90);
	}

	.image-wrapper {
		position: relative;
		width: 100%;
		aspect-ratio: 1/1; /* Perfect square */
	}

	.image {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		transition: opacity ease-in-out;
		opacity: 0;
	}

	.image.active {
		opacity: 1;
	}

	@media (max-width: 640px) {
		.dual-fader-container {
			gap: 10px;
		}
		.image-pair {
			width: calc(50% - 10px);
		}
	}

	.note {
		margin: 0 auto;
		max-width: 490px;
		width: 100%;
		border-top: solid 1px var(--brandGray);
	}

	.note p {
		font-family: OpenSans;
		font-weight: normal;
		color: var(--brandGray60);
		font-size: 12px;
		line-height: 18px;
		margin-top: 2px;
		margin-bottom: 0px;
		padding-top: 0px;
	}

</style>