<script>
	export let car = 0;
	export let transit = 0;
	export let walk = 0;
	export let bike = 0;
	
	const colors = {
		car: '#191919',
		transit: '#DC4633',
		walk: '#6FC7EA',
		bike: '#8DBF2E'
	};
	
	$: total = car + transit + walk + bike;
	$: segments = [
		{ width: total > 0 ? (car / total) * 100 : 0, color: colors.car, mode: 'Motor Vehicles' },
		{ width: total > 0 ? (transit / total) * 100 : 0, color: colors.transit, mode: 'Transit' },
		{ width: total > 0 ? (walk / total) * 100 : 0, color: colors.walk, mode: 'Walk' },
		{ width: total > 0 ? (bike / total) * 100 : 0, color: colors.bike, mode: 'Bicycles' }
	];
	
	$: segmentPositions = segments.reduce((acc, segment, i) => {
		const prevWidth = acc.length > 0 ? acc[i-1].end : 0;
		return [...acc, {
			start: prevWidth,
			end: prevWidth + segment.width,
			mid: prevWidth + (segment.width / 2),
			...segment,
			percentage: Math.round(segment.width) + '%'
		}];
	}, []);
</script>

<div class="bar-container">
	<svg class="stacked-bar">
		{#each segmentPositions as segment, i}
			<rect
				x={segment.start + '%'}
				y="0"
				width={segment.width + '%'}
				height="100%"
				fill={segment.color}
				stroke="white"
				stroke-width="0.5"
			/>
		{/each}
		{#each segmentPositions as segment, i}
			{#if segment.width > 1}
				<text
					x={segment.mid + '%'}
					y="35%"
					filter="url(#textGlow)"
					text-anchor="middle"
					dominant-baseline="middle"
					fill="white"
					font-family="OpenSans"
					font-size="14px"
					font-weight="normal">
					{segment.mode}
				</text>
				<text
					x={segment.mid + '%'}
					y="70%"
					text-anchor="middle"
					dominant-baseline="middle"
					font-family="OpenSansBold"
					font-weight="normal"
					fill="white"
					font-size="14px">
					{segment.percentage}
				</text>
			{/if}
		{/each}
	</svg>
</div>

<style>
	.bar-container {
		width: 100%;
		margin-top: -15px;
	}
	
	.stacked-bar {
		width: 100%;
		height: 40px;  /* Increased height to accommodate two lines of text */
		border-radius: 0px;
		overflow: visible;
	}
</style>