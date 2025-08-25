<script>
	export let car = 0;
	export let transit = 0;
	export let walk = 0;
	export let bike = 0;
	export let other = 0; 
	export let barHeight = "30px";
	
	const colors = {
		car: '#191919',
		transit: '#DC4633',
		walk: '#6FC7EA',
		bike: '#8DBF2E',
		other: '#D3D3D3'
	};
	
	$: total = car + transit + walk + bike + other;
	$: segments = [
		{ width: total > 0 ? (car / total) * 100 : 0, color: colors.car, mode: 'Motor Vehicles' },
		{ width: total > 0 ? (transit / total) * 100 : 0, color: colors.transit, mode: 'Transit' },
		{ width: total > 0 ? (walk / total) * 100 : 0, color: colors.walk, mode: 'Walk' },
		{ width: total > 0 ? (bike / total) * 100 : 0, color: colors.bike, mode: 'Bicycle' },
		{ width: total > 0 ? (other / total) * 100 : 0, color: colors.other, mode: 'Other' } 
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
	<svg class="stacked-bar" style="height: {barHeight}px;">
		{#each segmentPositions as segment}
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
		{#each segmentPositions as segment}
			{#if segment.width > 0.9}
				{#if segment.mode !== "Other"}
					<text
						x={segment.mid + '%'}
						y="35%"
						filter="url(#textGlow)"
						text-anchor="middle"
						dominant-baseline="middle"
						stroke="#191919"
						stroke-opacity=0.48
						stroke-width="3px"
						font-family="OpenSans"
						font-weight="normal">
						{segment.mode}
					</text>
					<text
						x={segment.mid + '%'}
						y="70%"
						text-anchor="middle"
						dominant-baseline="middle"
						stroke="#191919"
						stroke-opacity=0.48
						stroke-width="3px"
						font-family="OpenSansBold"
						font-weight="normal"
						fill="white"
						>
						{segment.percentage}
					</text>
					<text
						x={segment.mid + '%'}
						y="35%"
						filter="url(#textGlow)"
						text-anchor="middle"
						dominant-baseline="middle"
						fill="white"
						font-family="OpenSans"
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
						>
						{segment.percentage}
					</text>
				{/if}
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
		border-radius: 0px;
		overflow: visible;
	}

	text {
		font-size: 14px;
	}

	@media screen and (max-width: 500px) {
		text {
			font-size: 12px;
		}
	}

	@media screen and (max-width: 410px) {
		text {
			font-size: 10px;
		}
	}

</style>
