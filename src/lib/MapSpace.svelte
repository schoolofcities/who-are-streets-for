<script>

	import "../assets/global-styles.css";
	import 'leaflet/dist/leaflet.css';
	import { onMount } from 'svelte';
	import { browser } from '$app/environment';

	let map;
	let mapContainer;
	
	let L;
	const center = [43.67, -79.40];
	const zoom = 13;
	const tileLayerUrl = './space-tiles/{z}/{x}/{y}.png';

	onMount(async () => {

		if (browser) {

			L = await import('leaflet');
			
			map = L.map(mapContainer, {
				attributionControl: false,
				scrollWheelZoom: false,
				doubleClickZoom: false,
				boxZoom: false,
				keyboard: false,
				zoomControl: true
			}).setView(center, zoom);

			L.control.scale({ 
				position: 'bottomright',
				imperial: false, 
				metric: true 
			}).addTo(map);

			L.tileLayer(tileLayerUrl, {
				minZoom: 12,
				maxZoom: 16,
				tms: false,
			}).addTo(map);

		}

		return () => {
			if (map) {
				map.remove();
			}
		};
	});

</script>


<div class="legend-container">

	<h3>Mapping distribution of space in the City of Toronto</h3>

	<p>
		<svg width="40" height="15" xmlns="http://www.w3.org/2000/svg">
			<rect width="40" height="15" fill="black" stroke="#00A189" stroke-width="1" />
		</svg>
		Space for <strong>cars</strong> (roads, parking lots)
	</p>

	<p>
		<svg width="40" height="15" xmlns="http://www.w3.org/2000/svg">
			<rect width="40" height="15" fill="#00A189" stroke="#00A189" stroke-width="1"/>
		</svg>
		Space for <strong>people</strong> (sidewalks, paths, trails, plazas)
	</p>

	<p>
		<svg width="40" height="15" xmlns="http://www.w3.org/2000/svg">
			<rect width="40" height="15" fill="#d1f8f2" stroke="#00A189" stroke-width="1"/>
		</svg>
		Green space (parks, cemeteries, golf courses, school yards, ravines, hydro corridors, etc.) that to varying degrees are accessible to the public.
	</p>

</div>



<div class="map-container">

	<div class="map" bind:this={mapContainer}>

	</div>

	<p>
		Data from <a href="https://open.toronto.ca/" target="_blank">City of Toronto</a> and <a href="https://www.openstreetmap.org/#map=14/43.66710/-79.38875" target="_blank">OpenStreetMap</a>. Map data are from various collection periods (2019-2025) and may not reflect very recent changes to the built environment (e.g. Portlands redevelopment). Map created using QGIS and Leaflet.
	</p>

</div>



<style>

	.legend-container {
		margin: 0 auto;
		max-width: 680px;
		width: 100%;
		margin-top: 20px;
		margin-bottom: 20px;
		padding-left: 20px;
		padding-right: 20px;
		padding-top: 20px;
		border-top: solid 1px var(--brandGray);
	}

	.legend-container h3 {
		text-align: left;
		font-family: TradeGothicBold;
		font-weight: normal;
		margin-top: 0px;
		margin-bottom: 20px;
		font-size: 24px;
		color: var(--brandBlack);
	}

	.legend-container p {
		font-family: OpenSans;
		font-weight: normal;
		color: var(--brandGray90);
		font-size: 15px;
		line-height: 20px;
		margin-top: 2px;
		margin-bottom: 10px;
		padding-top: 0px;
	}

	.legend-container p strong {
		font-family: OpenSansBoldItalic;
		font-weight: normal;
	}

	.map-container {
		margin: 0 auto;
		margin-top: 20px;
		margin-bottom: 80px;
		width: 100%;
		max-width: 1440px;
		height: calc(75dvh);
		border-top: solid 1px var(--brandGray);
	}

	.map {
		height: 100%;
		width: 100%;
		border-bottom: solid 1px var(--brandGray);
		background-color: white;
	}

	.map-container p {
		font-family: OpenSans;
		font-weight: normal;
		color: var(--brandGray60);
		font-size: 12px;
		line-height: 18px;
		margin-top: 2px;
		margin-bottom: 0px;
		padding-top: 0px;
	}

	.map-container p a {
		font-family: OpenSans;
		font-weight: normal;
		color: var(--brandGray60);
		text-decoration: underline;
	}

	.map-container p a:hover {
		color: var(--brandBlack);
	}

	@media screen and (max-width: 1460px) {
		.map-container {
			margin-bottom: 90px;
		}
		.map-container p {
			padding-left: 20px;
			padding-right: 20px;
		}
	}
	@media screen and (max-width: 720px) {
		.map-container {
			margin-bottom: 100px;
		}
	}

	

</style>