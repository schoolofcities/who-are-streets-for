<script>

	import '../assets/global-styles.css';

	import Password from '$lib/Password.svelte';
	import Logo from '$lib/LogoTop.svelte';
	import TitleFullPage from '$lib/TitleFullPage.svelte';
	import TitleHalfSplit from '$lib/TitleHalfSplit.svelte';
	import TitleHalfSplitVideo from '$lib/TitleHalfSplitVideo.svelte';
	import TitleStandard from '$lib/TitleStandard.svelte';
	import AuthorDate from '$lib/AuthorDate.svelte';
	import ImageSingle from '$lib/ImageSingle.svelte';
	import VideoSingle from '$lib/VideoSingle.svelte';
	import GraphicSingle from '$lib/GraphicSingle.svelte';
	import GraphicsMultiples from '$lib/GraphicMultiples.svelte';
	import Footer from '$lib/Footer.svelte';

	import MapSpace from '$lib/MapSpace.svelte';
	import IntersectionImageFade from '$lib/IntersectionImageFade.svelte';
	import BarMode from '$lib/BarMode.svelte';

	
	// import Footnote from '$lib/Footnote.svelte';
    // import Footnotes from '$lib/Footnotes.svelte';
    // import { createFootnoteStore } from '$lib/footnoteUtils';

	// const footnoteStore = createFootnoteStore();
    // const { footnotes, addFootnote } = footnoteStore;

	// const fns = [
	// 	'Hello I am a footnote',
	// 	'Hello I am a second <a href="https://example.com" target="_blank">footnote</a> with a link',
	// 	'Author (Year) Publication information etc this might be a citation or a reference to a source',
	// 	'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas consequat lacus eu dolor dapibus sodales. Aenean venenatis metus id eleifend tincidunt. Nulla ut lacus et urna finibus bibendum sit amet et ante. Aliquam tristique, ex sed porttitor hendrerit, ex odio accumsan ex, eu maximus leo quam quis nulla.'
	// ];

</script>



<svelte:head>

	<title>Who Are Streets For? | School of Cities</title>

	<meta name="description" content="81% of street space in Toronto is inequitably dedicated to motor vehicles. How can this be fairly re-designed?" />
	<meta name="author" content="School of Cities">

	<meta property="og:title" content="Who are streets for?" />
	<meta property="og:description" content="81% of street space in Toronto is inequitably dedicated to motor vehicles. How can this be fairly re-designed?" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://schoolofcities.github.io/who-are-streets-for/" />
	<meta property="og:image" content="https://raw.githubusercontent.com/schoolofcities/who-are-streets-for/main/static/web-card.png" />
	<meta property="og:locale" content="en_CA">

	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="Who are streets for?" />
	<meta name="twitter:description" content="81% of street space in Toronto is inequitably dedicated to motor vehicles. How can this be fairly re-designed?" />
	<meta name="twitter:site" content="https://schoolofcities.github.io/who-are-streets-for/" />
	<meta name="twitter:image" content="https://raw.githubusercontent.com/schoolofcities/who-are-streets-for/main/static/web-card.png" /> 

</svelte:head>


<Password/>

<main>

	<!-- Full page title example -->

	<!-- <TitleFullPage
		title="Fun Captivating Project Title"
		subtitle="Maybe a slightly longer more detailed wordier project subtitle"
		image="https://jamaps.github.io/photos/picimgs/halifax2_2024.jpg"
		imageOpacity=0.9
		imageAltText="A photo"
		titleFontColour="var(--brandWhite)"
		subtitleFontColour="var(--brandWhite)"
		logoType="White"
	/> -->


	<!-- Here is a half split title example: -->

	<!-- <TitleHalfSplit
		title="Who are streets for?"
		subtitle="80% of street space in Toronto is inequitably dedicated to motor vehicles. How can this be fairly re-designed?"
		image="https://upload.wikimedia.org/wikipedia/commons/3/31/Victoria_Park_Avenue_at_Consumers_Road_in_Scarborough%2C_June_16_2025.jpg"
		imageAltText="A photo"
		titleFontColour="var(--brandWhite)"
		titleBorderColour="var(--brandYellow)"
		subtitleFontColour="var(--brandWhite)"
		backgroundColour="var(--brandGray90)"
		logoStyle="Dark"
	/> -->

	<TitleHalfSplitVideo
		title="Who are streets for?"
		subtitle="81% of street space in Toronto is inequitably dedicated to motor vehicles. How can this be fairly re-designed?"
		video="./video/college2.mp4"
		videoAltText="A photo"
		videoCaption="College St., Toronto."
		videoSource="Video by Geoffrey Anhorn."
		videoStart = 5
		videoSpeed = 1.5
		titleFontColour="var(--brandWhite)"
		titleBorderColour="var(--brandYellow)"
		subtitleFontColour="var(--brandWhite)"
		backgroundColour="var(--brandGray90)"
		logoStyle="Dark"
	/>
	
	<!-- Simple title example with logo and subtitle: -->

	<!-- <Logo logoType="Blue" backgroundColor="var(--brandWhite)"/>

	<ImageSingle
		imageURL="https://jamaps.github.io/photos/picimgs/taipei1_2025.jpg"
		caption="Taipei skyline."
		source="Jeff Allen."
		altText=""
		maxWidth="680px"
	/>

	<TitleStandard
		title="Fun Captivating Project Title"
		subtitle="Maybe a slightly longer more detailed wordier project subtitle "
	/> -->

	<div class="text">

		<AuthorDate
			authors="<a href='' target='_blank'>Jeff Allen</a>, <a href='' target='_blank'>Lanrick Bennit Jr.</a>, <a href='' target='_blank'>Mia Wang</a>"
			date="September 2025"
		/>

		<div class="caption-container" style="margin-top: -25px; margin-bottom: 25px;">
			<p style="font-size: 13.7px; color: #4d4d4d">
				<span class="caption-text"><i>Jeff Allen led the mapping and data analysis; Lanrick Bennet Jr. led the majority of the writing and contextual research; Mia Wang provided data collection and analysis support.</i></span>
			</p>
			<br>
		</div>

		<p>
			Walk down almost any Toronto street and it becomes clear who it’s built for. Sidewalks are narrow, often cracked or cluttered with utility poles and sandwich boards. Protected bike lanes and dedicated surface transit routes remain limited and disconnected. Meanwhile, multi-lane roads dominate the urban landscape, often surrounded by a sea of parking lots. 
		</p>
		<p>
			What if we asked a simple question: who is all this space really for?

		</p>
		<p>
			The answer, backed by a close look at the data and geography, reveals deep inequities in how Toronto allocates outdoor space. Whether you walk, bike, take transit or drive, the way public land is distributed has serious implications for how we move, how safe we feel, and who can access opportunities in this city.
		</p>
		<p>
			This city-wide map shows it clearly: roads and surface parking lots dominate Toronto’s public realm in most neighbourhoods. In total, more than 125 square kilometres of land in Toronto is dedicated to motor vehicles (approximately 20% of the City's total land area) – that's over 360 Trinity Bellwoods Parks.
		</p>

	</div>

	<MapSpace />

	<div class="text">

		<h2 style="padding-top: 30px;">
			A disconnect between space and travel patterns
		</h2>
		<p>
			The following map shows every transportation segment in Toronto: streets, highways, laneways, sidewalks, paths, trails, and public transit routes.
		</p>
		
	</div>

	<ImageSingle
		imageURL="./images/all-transport-corridors.png"
		caption=""
		altText="Map of all transportation corridors in Toronto."
		maxWidth="720px"
		link="No"
	/>

	<div class="text">

		<p>
			For each of these segments, we combined <a href="https://open.toronto.ca/catalogue/?search=topographic%20mapping&sort=score%20desc" target="_blank">City of Toronto</a> and <a href="https://www.openstreetmap.org/#map=14/43.66710/-79.38875" target="_blank">OpenStreetMap</a> data to estimate the total area allocated to the four main modes in which people travel: walking (e.g. sidewalks), bicycling (e.g. bike lanes), public transit (e.g. dedicated transit lanes), and driving (motor vehicle lanes and on-street parking). Here are examples of how this data looks relative to satellite imagery in a couple locations.
		</p>

		<IntersectionImageFade
			image1="./images/intersection-eglinton-beachell-sat.png"
			image2="./images/intersection-eglinton-beachell-schematic.png"
			image3="./images/intersection-greenwood-dundas-sat.png"
			image4="./images/intersection-greenwood-dundas-schematic.png"
			duration={3500}
			title1="Eglinton Ave. E & Beachell St."
			title2="Greenwood Ave. & Dundas St. E"
			note="Two examples of estimating street area allocated for each of the four main travel modes in Toronto. Spaces used by multiple modes (e.g. transit routes that run in mixed traffic, pedestrian crossings) are coded to the most dominant mode. Data sources: City of Toronto and OpenStreetMap."
		/>

		<p>
			Summing this data across the entire City of Toronto, we find that the vast majority of space on these segments is allocated to motor vehicles, with cycling and dedicated public transit routes only receiving only a small fraction of the space.  
		</p>
		

		<h4>
			Area of transportation infrastructure in the City of Toronto allocated to each travel mode
		</h4>

		<BarMode
			car={81}
			transit={2}
			walk={15}
			bike={2}
			other={0}
			barHeight={40}
		/>

		<p>			
			These inequalities are especially notable when we compare them with <a href="https://dmg.utoronto.ca/tts-introduction/" target="_blank">Transportation Tomorrow Survey</a> data on how City of Toronto residents typically travel. 
		</p>
		<p>
			This imbalance stems from decades of political, planning, and engineering decisions which have prioritized motor vehicles over people. 
		</p>

		<h4>
			Percent of trips by City of Toronto residents taken by travel mode
		</h4>

		<BarMode
			car={56}
			transit={18}
			walk={21}
			bike={3}
			other={2}
			barHeight={40}
		/>

		<h4>
			Percent of local trips by City of Toronto residents taken by travel mode
		</h4>

		<BarMode
			car={49}
			transit={13}
			walk={33}
			bike={4}
			other={2}
			barHeight={40}
		/>

		<div class="caption-container">
			<p>
				<span class="caption-source">
					<i>Data notes:</i> Local trips encompass all trips {"<5km"}. Trips are grouped by the primary mode of each trip (e.g. a trip where someone is driven to a subway station, takes the subway, and then walks to their final destination is classified as "Transit"). Since the majority of trips include walking (e.g. to/from transit, to/from parking a car are bicycle, etc.), the % of trips by walking is likely under-estimated. About 2% of trips are taken by 'Other' modes (e.g. school bus, motorcycle, e-scooter, etc.) that are not shown for sake of brevity.
				</span>
			</p>
		</div>

		<p>
			This mismatch is geographically even. The maps below show the difference, by City ward, between how much space is allocated to each travel mode, and how residents of those wards actually travel. Some patterns emerge, most notably that downtown and older adjacent wards are the most overly designed for motor vehicles, relative to how residents actually travel. They also have the greatest difference in space allocated to active modes, walking and bicycling, relative to how often people travel via these modes.  These maps were partly inspired by similar <a href="https://doi.org/10.1016/j.jcmr.2025.100071" target="_blank">research in Montreal</a>, that also showed centralization of greater mismatch in micromobility (i.e. bicycling).
		</p>

	</div>

	
	<GraphicsMultiples

		svgPaths={[
			"./images/mode-map-car-360.svg",
			"./images/mode-map-transit-360.svg",
			"./images/mode-map-walk-360.svg",
			"./images/mode-map-cycling-360.svg"
		]}

	/>


	<div class="text">

		<div class="caption-container">
			<p>
				<span class="caption-source">
					These maps show just one way for helping to prioritize new infrastructure (mismatch of supply and demand), but there are other important factors as well (safety, equity, air quality, cost, network connectivity, etc.) that are often considered by transportation planners and engineers.
					<br><br>
					For these maps, the data on mode share and space allocation were linked to Wards via areal interpolation. For travel mode share data, this was originally collected at smaller neighbourhood-sized zones. For more maps on how people travel in the Toronto region at this smaller zonal level, check out our <a href="https://schoolofcities.github.io/transportation-tomorrow-survey/" target="_blank">interactive map</a>.
				</span>
			</p>
		</div>

		<br>

		<h2>
			Glimpses of a better future
		</h2>

		<p>
			Toronto has already implemented a number of low-cost interventions to re-balance our streets, from CaféTO patios to pilot bike lanes and seasonal road closures. These glimpses of a better future highlight what’s possible when space is shared more equitably. The status quo, by contrast, produces clear harms: unsafe streets where traffic violence is normalized, high emissions from the city’s second-largest source of greenhouse gases, and inequities that privilege those who can afford private vehicles over those who cannot. Despite car dominance of street space, many residents still choose to walk (33%), bicycle (4%), or ride public transit (13%) for trips under five kilometres. That suggests that if more space were allocated to these modes, Toronto would not only reduce inequalities but also likely see significant mode shift.
		</p>

		<h3>
			Dedicated surface transit lanes
		</h3>

		<p>
			Despite decades of car-based planning, there are examples of how Toronto is starting to reallocate space for public transit. For example, in Scarborough, dedicated bus lanes have been added to Eglinton Ave. E, Kingston Rd., and Morningside Ave. as part of the City's <a href="https://www.toronto.ca/services-payments/streets-parking-transportation/transportation-projects/rapidto/" target="_blank">RapidTO surface transit network plan</a>.
		</p>

	</div>


	<ImageSingle
		imageURL="./images/kingstonrd.jpg"
		caption="Painted bus lanes on Kingston Rd. in West Hill, Scarborough, July 2025."
		source="Wikimedia Commons."	
		altText=""
		maxWidth="680px"
		link="Yes"
	/>

	<div class="text">

		<p>
			These bus lanes have been shown to <a href="https://www.toronto.ca/wp-content/uploads/2025/07/964b-RapidTO-Eglinton-East-Dashboard-Jan-2022-to-Mar-2023Dec5v2r.pdf" target="_blank">improve travel times and reliability for transit users</a>. They are a clear example of how reallocating space can benefit everyone, not just those who drive.
		</p>
		<p>	
			Similarly, the King Street Transit Priority Corridor in downtown Toronto, a globally recognized success, was fundamentally an exercise in reallocating road space from low-occupancy private vehicles to high-capacity streetcars. By making transit the primary focus, the project moves tens of thousands of people daily <a href="https://www.toronto.ca/services-payments/streets-parking-transportation/transportation-projects/king-street-pilot/data-reports-background-materials/" target="_blank">more efficiently and reliably than before</a>.
		</p>
		<p>
			Toronto has approximately <strong>1,300 kilometres</strong> of highways, major arterial roads, and minor arterial roads. The vast majority of these roads have TTC surface transit routes and have ample space to add dedicated bus or streetcar lanes to improve transit reliability and travel times. These roads will not truly be effective "arteries" until they are designed to prioritize people who ride public transit, instead of only motor vehicles.
		</p>

	</div>

	<!-- <ImageSingle
		imageURL="./images/major-roads-surface-transit-options.png"
		caption=""
		source=""	
		altText=""
		maxWidth="1080px"
		link="No"
	/> -->

	<GraphicSingle
		svg1080="./images/corridor-map-1080.svg"
		svg720="./images/corridor-map-720.svg"
		svg360="./images/corridor-map-360.svg"
	/>

	<div class="text">

		<p>
			Extrapolating from <a href="https://www.toronto.ca/services-payments/streets-parking-transportation/transportation-projects/rapidto/rapidto-bus-lanes/eglinton-east-bus-lanes/", target="_blank">City of Toronto reports of recent costs of bus lanes in Scarborough</a> (<strong>$470,000 / km</strong>), adding dedicated transit lanes to half of the City's highway and arterial road network would cost approximately <strong>$305 million</strong>. This is quite low when compared to the <a href="https://schoolofcities.utoronto.ca/wp-content/uploads/2025/04/Understanding-the-Drivers-of-Transit-Construction-Costs-in-Canada_Feb-2025_FINAL.pdf" target="_blank">rising costs of larger public transit infrastructure projects</a> across Canada. 
			For example, the most recent cost estimate for the three-stop Scarborough Subway Extension is <strong><a href="https://www.thestar.com/news/gta/metrolinx-says-scarborough-subway-extension-budget-has-doubled-offers-little-update-on-progress/article_0d063e6b-2a44-4e53-9d43-7919171830ab.html" target="_blank">$10.2 billion</a></strong> (<strong>$1,300,000,000 / km</strong>). This is not to say that dedicated surface transit lanes are a replacement for higher capacity public transit projects, but rather that they are a cost-effective way to improve transit service quickly and to provide connections to potentially all neighbourhoods in the city.
		</p>

		<p>	
			To be as successful as possible, surface transit routes also require the implementation of measures such as transit-priority signals and enforcement against illegal parking in dedicated transit lanes.
		</p>

	</div>

	<div class="text">

		<h3>
			Converting unproductive on-street parking to better uses
		</h3>

		<p>
			On-street parking isn't free. Street parking might seem like a minor detail in how we plan urban space, but it plays an outsized role in limiting how streets can be used. In many parts of Toronto, curb lanes are dedicated to vehicle storage parking, despite being some of the most valuable real estate in the city.
		</p>

		<p>
			In the core, the costs go beyond opportunity. A <a href="https://uttri.utoronto.ca/wp-content/uploads/sites/19/2017/09/Impacts-of-Illegal-On-Street-Parking-on-Torontos-CBD-Congestion.pdf"  target="_blank">University of Toronto report</a> found that illegal on-street parking, including in no-parking zones, or double-parking, “reduces lane capacity and disrupts traffic flow, particularly during peak hours.” Their study found that even relatively short parking violations in the Financial District led to measurable increases in congestion and delays for all road users. Moreover, as <a href="https://www.theglobeandmail.com/opinion/editorials/article-the-hidden-costs-of-cheap-parking/" target="_blank">the Globe and Mail editorial board</a> noted, “road space at the curb is a valuable and limited commodity,” and giving it away for cheap reflects “bad economics and bad politics”. 
		</p>



		<p>
			So how can on-street parking be converted to better uses?
		</p>

		<p>
			A visible example is <a href="https://www.toronto.ca/business-economy/business-operation-growth/business-support/cafeto-outdoor-dining/" target="_blank">CaféTO</a>, which has repeatedly demonstrated how curb lanes can be transformed from storage for a single idle vehicle into vibrant patios serving dozens of people, acting as a lifeline for local restaurants and creating new social hubs. The City has also formalized this concept through its  <a href="https://www.toronto.ca/wp-content/uploads/2019/08/949e-Cafe-Application-Package-Final.pdf"  target="_blank">Parklet Program</a>, which provides official guidelines for converting individual parking spots into mini public parks, complete with seating and greenery, proving that even small-scale interventions can inject life and community onto a street. Climate resilience is improved by reclaiming pavement; through its <a href="https://www.toronto.ca/services-payments/streets-parking-transportation/enhancing-our-streets-and-public-realm/green-streets/green-infrastructure-resources/"  target="_blank">Green Infrastructure program</a>, Toronto is now building <a href="https://www.toronto.ca/wp-content/uploads/2021/08/8e5e-ecs-specs-gi-dwgs-T-850.111-Rev0-Sep2021.pdf"  target="_blank">bioswales</a> in the space once occupied by asphalt curb lanes to absorb stormwater and provide green space to neighbourhoods.
		</p>

	</div>
		
	<ImageSingle
		imageURL="./images/palmerston.jpg"
		caption="Green buffer and contra-flow bike lane on Palmerston Ave. just north of College St."
		source="<br>Photo by Jeff Allen, August 2025"	
		altText=""
		maxWidth="680px"
		link="Yes"
	/>

	<ImageSingle
		imageURL="./images/tecumseth.jpg"
		caption="Protected bicycle lane and newly planted green buffer on Tecumseth St. just south of King St."
		source="<br>Photo by Jeff Allen, August 2025"	
		altText=""
		maxWidth="680px"
		link="Yes"
	/>

	<div class="text">

		<p>
			This principle of reallocation has been scaled up with transformative results for transportation. Along major corridors like <a href="https://www.toronto.ca/explore-enjoy/parks-recreation/activeto/activeto-expanding-the-cycling-network/" target="_blank">Bloor St., University Ave., Danforth Ave., and Yonge St.</a>, the installation of protected bike lanes came from directly repurposing space previously dedicated to on-street parking. This represented a clear policy choice: prioritizing the safe movement of thousands of cyclists over the storage of a few dozen cars.
		</p>

		<p>
			What about the costs? Funds from strategies like demand-based parking pricing, increased traffic enforcement, and congestion charges could each generate ample revenue to re-design Toronto streets.
		</p>

		<p>
			Toronto recently eliminated parking minimums and even introduced maximums to curb overbuilding – a positive shift. But curbside parking remains largely untouched. Most spaces are still free or underpriced, treated as a public entitlement rather than a scarce resource. As <a href="https://en.wikipedia.org/wiki/Donald_Shoup" target="_blank">Donald Shoup</a> and others have long argued, cheap parking is a subsidy that encourages driving, worsens congestion, and prevents curbspace from being reallocated to higher-value uses like bike lanes, transit priority, green buffers, or delivery zones. Until Toronto embraces demand-based pricing, the street remains a free bonus for drivers, reinforcing inequality in how public space is shared.
		</p>

		<p>
			Better enforcement, particularly via automated cameras, could also lead to substantial revenue. <a href="https://schoolofcities.github.io/king-street-toronto/traffic-violations" target="_blank">Our previous research found that lack of enforcement on the King St.</a> is leading to about <strong>$750,000</strong> of lost revenue per day on King St. alone, based on data from the City of Toronto and Toronto Police.
		</p>

		<p>	
			
			In <a href="https://schoolofcities.utoronto.ca/could-congestion-pricing-unlock-a-better-toronto/" target="_blank">other previous research we estimated the potential income of congestion pricing</a> and found that, based on recent travel survey data, a $9 fee for driving into central Toronto would generate over <strong>$2 million</strong> per day in revenue. 
		</p>

	</div>


	<div class="text">

		<h3>
			Open Streets: Reclaiming roads for people
		</h3>

		<p>
			Open Streets programs flip the script on who streets are really for. Instead of prioritizing cars, these events temporarily close major roads to traffic and invite people to walk, bike, roll, dance, or simply gather. The impact is immediate: streets become safe, sociable, and vibrant.
		</p>

		<VideoSingle
			videoURL="./video/connaught.mp4"
			caption="Connaught School Open Street in Calgary, Alberta. An example of a community-led open street"
			source="Video by Kosta Diochonos, School of Cities. <a href='https://www.instagram.com/reel/DNQ6ECVtQsx/?igsh=N3p0bmw5enZtYWd3' target='_blank'>Instagram</a></VideoSingle> / <a href='https://vt.tiktok.com/ZSSvUufYv/' target='_blank'>TikTok</a></VideoSingle>"
			altText="Short demo video"
			maxWidth="340px"
			playbackRate={1}
			showControls={false}
		/>

		<p>
			<a href="https://www.openstreetsto.org/" target="_blank">Toronto’s Open Streets</a> program, which began as a small pilot in 2014, has shown glimpses of what’s possible. On Yonge St. and Bloor St., families, newcomers, and seniors alike have filled the roadways, discovering how much more welcoming the city feels without car traffic dominating every metre of space. Although these events remain limited in duration and frequency, they highlight a demand for streets that support community life, not just vehicle flow.
		</p>




		<p>
			What’s more, Toronto already has the tools to go further. In 2025, the City and the Toronto Association of Business Improvement Areas (TABIA) released <a href="https://www.toronto-bia.com/wp-content/uploads/2025/06/Pedestrian-Streets-BIA-June-10-2025.pdf" target="_blank">Pedestrian Streets: Policy & Guidelines Development</a>, offering BIAs and neighbourhoods a roadmap for transforming roadways into pedestrian-friendly public spaces. So far, however, these initiatives have mostly been tied to street festivals and short-term pilots, rather than sustained or seasonal transformations. Market St., next to the St. Lawrence Market, is one exception, a seasonal open street which began as a pilot in summer 2021. 
		</p>

	</div>

	<ImageSingle
		imageURL="./images/market-st.jpg"
		caption="Market St., Toronto."
		source="<br>Photo by Lanrick Bennet Jr., August 2025"	
		altText=""
		maxWidth="680px"
		link="Yes"
	/>

	<div class="text">

		<p>
			Other cities have demonstrated what happens when these programs scale up. In Bogotá, the world-renowned <a href="https://www.researchgate.net/publication/45629811_The_Ciclovia-Recreativa_A_Mass-Recreational_Program_With_Public_Health_Potential#:~:text=The%20Ciclov%C3%ADa%2DRecreativa%20is%20a,%2C%20rollerbladers%2C%20and%20cyclists%20only." target="_blank">Ciclovía</a> engages millions each Sunday and is credited with delivering more than three dollars in public health benefits for every dollar invested. Montreal, meanwhile, has reimagined Open Streets into a seasonal tradition: each summer, <a href="https://www.cbc.ca/news/canada/montreal/pedestrian-streets-summer-1.7544589" target="_blank">avenues like Mont-Royal and Wellington</a> transform into <a href="https://montreal.ca/en/articles/pedestrian-streets-liven-city-summer-31971" target="_blank">pedestrian promenades</a> filled with patios, art, and performances. In 2025, the city went further by permanently pedestrianizing a stretch of <a href="https://www.cbc.ca/news/canada/montreal/ste-catherine-east-pedestrian-street-1.7615675" target="_blank">Ste-Catherine St. E</a> in the Village, adding trees, green space, and public seating to create a cultural hub year-round.
		</p>

	</div>


	<ImageSingle
		imageURL="./images/mtl/mtl-photos.png"
		caption="Open streets in Montreal"
		source="<br>Photos by Patrick Murphy (Oh The Urbanity!)"	
		altText=""
		maxWidth="1080px"
		link="Yes"
	/>

	<div class="text">

		<p>
			In Toronto, scaling up Open Streets would require political will more than money. The city already has the infrastructure, a policy framework, and organizational know-how, and public demand for safe, people-friendly streets is clear. Making these transformations of the public realm more frequent and expanding them to additional neighbourhoods could help rebalance inequities in who gets to use our most valuable public space. 
		</p>

		<h2>
			Residents are supportive of change
		</h2>

		<p>
			Surveys in Toronto have also consistently shown that most residents want more space for walking, bicycling, and public transit.
		</p>
		<p>
			For example, in Scarborough, a region often labeled as car-dependent, <a href="https://doi.org/10.1016/j.trd.2024.104514" target="_blank">University of Toronto research led by Ignacio Tiznado-Aitken</a>, Assistant Professor in Geography and Planning, asked residents which moded should receive the priority for space and investment. Comparing this to how space is currently allocated in Scarborough highlights a stark disconnect between what people want and what has been built.
		</p>

		<h4>
			Percent of space allocated to each travel mode in <u>Scarborough</u>
		</h4>

		<BarMode
			car={83}
			transit={1}
			walk={15}
			bike={1}
			other={0}
			barHeight={40}
		/>

		<h4>
			Survey of <u>Scarborough</u> residents on which mode should have the "highest priority in terms of space and investment"
		</h4>

		<BarMode
			car={32}
			transit={42}
			walk={19}
			bike={7}
			other={0}
			barHeight={40}
		/>

		<p>
			Moreover, when the City of Toronto proposes new street designs, their survey responses are typically very supportive. For example, <a href="https://www.toronto.ca/legdocs/mmis/2023/te/bgrd/backgroundfile-237354.pdf" target="_blank">90% of survey respondents were supportive for pedestrian-only zones in Kensington Market</a>. <a href="https://www.toronto.ca/wp-content/uploads/2025/07/8e69-RapidTO-Bathurst-Consultation-Report.pdf" target="_blank">Nearly 70% of survey respondents agreed that major roads, such as Bathurst St., should prioritize moving people by public transit</a>, from a recent survey of proposed transit-priority lanes. Even the most politically controversial bike lanes have majority support. For example, <a href="https://www.toronto.ca/wp-content/uploads/2023/05/9871-TTWBloorStW-ConsultationSummaryReport-2023-04-19AODA.pdf" target="_blank">more than 50% of surveyed residents were supportive of bike lanes on Bloor St. W</a> (between Runnymede Rd. and Resurrection Rd.).
		</p>

		<p>
			The minority opposition to street re-designs and reduction of parking is sometimes framed around concerns of customer access and deliveries to businesses. But deliveries could be adjusted to mornings or late at night. While the amount of customers arriving by motor vehicles is often over-estimated by merchants. In Toronto, after bike lanes were installed along Bloor St. in the Annex and Koreatown, the percent of visitors who arrived by car did not change significantly, and overall people were <a href="https://tcat.ca/wp-content/uploads/2019/09/Bike-Lanes-and-Business-on-Bloor-Snapshot-2019-09-04.jpg" target="_blank">spending more</a>.
		</p>

	</div>


	<div class="text">
		
		<h2>
			Political and psychological challenges
		</h2>

		<p>
			So if there is overall support for street re-design projects when they are proposed, and the data of recent projects show overwhelming positives for transit riders and active travel with little detriment to motor vehicle travel times, then why are changes limited to a few case studies and disconnected sections? Or when changes do happen, why is implementation often riddled with compromises which limit their potential effectiveness?  
		</p>

		<p>	
			Cost should not be a barrier since as we've noted, the cost of prioritizing surface public transit, reallocating on-street parking, and opening streets is relatively quite small – especially when compared to major infrastructure projects. Moreover, costs could be covered by increased enforcement.
		</p>

		<p>
			A major challenge is shifting from the political status quo, which greatly favours those with access to private motor vehicles and maintains infrastructure that privileges their convenience over equity and community benefit. As <a href="https://spacing.ca/toronto/2024/11/27/the-high-cost-of-on-street-parking/" target="_blank">John Lorinc writes in Spacing</a>, “Toronto needs to confront the reality that curbside real estate is a limited and highly contested resource. Yet, in many places, we still treat it like an entitlement.” Decisions about street space aren’t neutral or technical, they reflect political choices. What could otherwise support bike lanes, patios, green buffers, or loading zones is instead handed over, often at low cost, for drivers to leave their cars idle.
		</p>

		<p>
			Policies that reduce car dominance are often perceived as unreasonable, not because of data or evidence, but because of a widespread assumption that driving must remain the default mode of transport. Recent research has framed this as <strong>motonormativity</strong>, which refers to the deep cultural bias that treats car use as normal, necessary, and morally neutral, despite having detrimental safety, equity, and environmental impacts. This bias, shaped by decades of media, built infrastructure, and policy leads many people to apply a different standard of judgment to driving than they would to comparable behaviours. For example, <a href="https://doi.org/10.1504/IJENVH.2023.135446" target="_blank">research in the UK</a> found that most people opposed exposing others to secondhand smoke, but many accepted toxic car fumes on crowded streets without question. This double standard makes it politically difficult to reallocate road space toward public transit, cycling, and walking even when such changes would improve public health, safety, and sustainability.
		</p>

		<p>
			Similarly, people often over-estimate how many people travel by car, likely because they simply take up more space, which can further skew biases. For example, when bike lanes were being installed on Bloor St. in the Annex and Koreatown, <a href="https://tcat.ca/wp-content/uploads/2019/09/Bike-Lanes-and-Business-on-Bloor-Snapshot-2019-09-04.jpg" target="_blank">over half of merchants believed that 25% or more of their customers arrived by car, but the reality was that less than 10% of visitors arrived by car on average.</a>
		</p>

		<p>
			Another possible barrier to change is <strong>pluralistic ignorance</strong>, a social psychology concept where people individually reject a norm or belief, but incorrectly assume that most others accept it. This can lead to the norm appearing stronger than it actually is. For example, <a href="https://doi.org/10.1016/j.gloenvcha.2025.102980">recent research on motonormativity</a> found that many people assumed that other people’s support for non-car transport was lower than their own support, which could lead to less political action than what people want. This research finding, combined with surveys of residents, shows that ample support for public transit and active travel is there, it just needs to be unlocked with increased evidence, advocacy, implementation, and political will.
		</p>

	</div>

	<div class="text">

		<h2>
			A fairer future is one we design
		</h2>

		<p>
			Public space belongs to everyone, not just car owners. For too long, Toronto’s streets have served vehicles first. But as we've seen, this is not inevitable. The choice to rebalance our streets is already underway. The successes of CaféTO, the King St. transit corridor, and new protected bike lanes are not isolated experiments; they are a clear verdict. They prove that when we reclaim space from idle cars, we create more room for people, for community, and for a more resilient city.
		</p>
		
		<p>
			The path forward is to make this the rule, not the exception. We can achieve this by implementing smart policies and cost-effective re-designs that treat our land as the valuable public asset it is. This means decisively reallocating on-street parking to create permanent space for wider sidewalks, safer bike lanes, and dedicated surface public transit routes. It means pricing our curb lanes to manage demand and reinvesting that revenue directly into the neighbourhood improvements residents are asking for: better transit, pedestrian, and cycling infrastructure and vibrant street-scapes and public spaces. 
		</p>
		
		<p>
			Imagine walking down a curb that is not a lane of cars, but a widened sidewalk filled with planters. Imagine biking on a protected lane unblocked by parked vehicles, or catching a bus that arrives on time because its path is clear.	This isn't a distant dream. When we choose to design streets for people, we build a safer, greener, and more equitable Toronto for everyone, starting with the public space that actually serves all its residents.
		</p>
		
		<br>

		<div class="details">

			<h2>Acknowledgements</h2>

			<p>
				We would like to thank OpenStreetMap contributors as well as the City of Toronto for sharing open data that allowed for the analysis; Andy Woodruff and Daniel Romm who created excellent maps of other cities that inspired parts of this project; Geoffrey Anhorn and Kosta Diochnos for providing videos; and Felicity Heyworth for editing.
			</p>

		</div>
		
    </div>

	

	<Footer />

</main>


