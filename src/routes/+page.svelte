<script>

	import '../assets/global-styles.css';

	import Password from '$lib/Password.svelte';
	import Logo from '$lib/LogoTop.svelte';
	import TitleFullPage from '$lib/TitleFullPage.svelte';
	import TitleHalfSplit from '$lib/TitleHalfSplit.svelte';
	import TitleStandard from '$lib/TitleStandard.svelte';
	import AuthorDate from '$lib/AuthorDate.svelte';
	import ImageSingle from '$lib/ImageSingle.svelte';
	import GraphicSingle from '$lib/GraphicSingle.svelte';
	import GraphicsMultiples from '$lib/GraphicMultiples.svelte';
	import Footer from '$lib/Footer.svelte';

	import MapSpace from '$lib/MapSpace.svelte';
	import IntersectionImageFade from '$lib/IntersectionImageFade.svelte';
	import BarMode from '$lib/BarMode.svelte';

	
	import Footnote from '$lib/Footnote.svelte';
    import Footnotes from '$lib/Footnotes.svelte';
    import { createFootnoteStore } from '$lib/footnoteUtils';

	const footnoteStore = createFootnoteStore();
    const { footnotes, addFootnote } = footnoteStore;

	const fns = [
		'Hello I am a footnote',
		'Hello I am a second <a href="https://example.com" target="_blank">footnote</a> with a link',
		'Author (Year) Publication information etc this might be a citation or a reference to a source',
		'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas consequat lacus eu dolor dapibus sodales. Aenean venenatis metus id eleifend tincidunt. Nulla ut lacus et urna finibus bibendum sit amet et ante. Aliquam tristique, ex sed porttitor hendrerit, ex odio accumsan ex, eu maximus leo quam quis nulla.'
	];

</script>



<svelte:head>

	<title>Who Are Streets For? | School of Cities</title>

	<!-- <meta name="description" content="Repository of design and web components for building data stories, visualizations, maps, and other custom web projects" />
	<meta name="author" content="Jeff Allen">

	<meta property="og:title" content="Design Components" />
	<meta property="og:description" content="Repository of design and web components for building data stories, visualizations, maps, and other custom web projects" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://schoolofcities.github.io/design-components/" />
	<meta property="og:image" content="https://raw.githubusercontent.com/schoolofcities/design-components/main/static/web-card.png" />
	<meta property="og:locale" content="en_CA">

	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="Design Components" />
	<meta name="twitter:description" content="Repository of design and web components for building data stories, visualizations, maps, and other custom web projects" />
	<meta name="twitter:site" content="https://schoolofcities.github.io/design-components/" />
	<meta name="twitter:image" content="https://raw.githubusercontent.com/schoolofcities/design-components/main/static/web-card.png" />  -->

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

	<TitleHalfSplit
		title="Who are streets for?"
		subtitle="80% of street space in Toronto is inequitably dedicated to cars. How can this be fairly re-designed?"
		image="https://upload.wikimedia.org/wikipedia/commons/3/31/Victoria_Park_Avenue_at_Consumers_Road_in_Scarborough%2C_June_16_2025.jpg"
		imageAltText="A photo"
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
			authors="<a href='' target='_blank'>Jeff Allen</a> & <a href='' target='_blank'>Lanrick Bennit Jr.</a>"
			date="August 2025"
		/>

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
			This city-wide map shows it clearly: roads and surface parking lots dominate Toronto’s public realm in most neighbourhoods. In total, ___km<sup>2</sup> of land in Toronto is dedicated to cars, that's over ___ Trinity Bellwoods Parks.
		</p>
		<!-- <p>
			Nunc vel massa turpis. Vivamus id odio ut nulla dignissim molestie. <Footnote id={addFootnote(fns[1])} />
		</p> -->
	</div>

	<MapSpace />

	<div class="text">

		<h2>
			A disconnect between space and travel patterns
		</h2>
		<p>
			The following map shows every transportation segment in Toronto; streets, highways, laneways, sidewalks, paths, trails, and public transit routes.
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
			For each of these segments, we combined data to estimate the total area allocated to the four main modes in which people travel: walking (e.g. sidewalks), bicycling (e.g. bike lanes), public transit (e.g. dedicated transit lanes), and driving (motor vehicle lanes and on-street parking). Here are examples of how this data looks relative to satellite imagery in a couple locations.
		</p>

	</div>

	
	<IntersectionImageFade
		image1="./images/intersection-eglinton-beachell-sat.png"
		image2="./images/intersection-eglinton-beachell-schematic.png"
		image3="./images/intersection-eglinton-beachell-sat.png"
		image4="./images/intersection-eglinton-beachell-schematic.png"
		duration={2500}
		title1="Eglinton Ave. East & Beachell St."
		title2="Eglinton Ave. East & Beachell St."
		note="Data for . . Dedicated transit. If multiple modes overlap, the area is counted for the dominant mode."
	/>

	<div class="text">

		<p>
			Summing this data across the entire City of Toronto, we find that the vast majority of space on these segments are allocated to motor vehicles, with cycling and dedicated public transit routes only receiving only a small fraction of the space. 
		</p>
		<p>			
			These inequalities are especially notable when we compare with <a href="https://dmg.utoronto.ca/tts-introduction/" target="_blank">Transportation Tomorrow Survey data</a> on how people typically travel. 
		</p>

		<h4>
			Percent of transportation infrastructure in the City of Toronto allocated to each travel mode
		</h4>

		<BarMode
			car={80}
			transit={3}
			walk={15}
			bike={2}
		/>

		<h4>
			Percent of trips by City of Toronto residents taken by travel mode
		</h4>

		<BarMode
			car={56}
			transit={18}
			walk={21}
			bike={3}
		/>

		<h4>
			Percent of local trips by City of Toronto residents taken by travel mode
		</h4>

		<BarMode
			car={49}
			transit={13}
			walk={32}
			bike={4}
		/>

		<p>
			This imbalance stems from decades of political, planning, and engineering decisions which have prioritized motor vehicles over people. 
			<!-- It shapes so much of what people experience outside our cars and makes walking or biking feel precarious, even when it's already how many people prefer to move. -->
		</p>

		<p>
			LANRICK TEXT WHY ALLOCATING SO MUCH SPACE FOR CARS IS BAD
		</p>

		<p>
			<i>BEGIN TRANSISSION FROM NEGATIVE TO POSITIVE, PROBLEM TO SOLUTION</i>
		</p>

	</div>


	<div class="text">

		<h2>
			Glimpses of a better future
		</h2>

		<p>
			Toronto already has implemented a number of low-cost options for re-designing our streets. These can help re-balance inequalities of space allocated to different travel modes and .... LANRICK ADD TEXT FOR WHY DOING SO IS IMPORTANT FOR EQUITY, CLIMATE, SAFETY, HAPPINESS, RESILIANCE, ETC.
		</p>
		<p>
			A positive of our findings above is that even though it accounts for a very small minority of space, many residents, for various reasons, opt to walk, cycle, or take transit, indicating that if more space were allocated for these modes, it would not only reduce inequalities, but likely lead to mode shifting as well. REWORD THIS?? 
		</p>

		<h3>
			Dedicated surface transit lanes
		</h3>

		<p>
			Despite decades car-based planning, there are examples of how Toronto is starting to reallocate space for public transit. For example, in Scarborough, dedicated bus lanes have been added to Eglinton Ave. East, Kingston Rd., and Morningside Ave. 
			<!-- These were implemented at a relatively low cost, <strong>$4 Million</strong> according to <a href="https://www.toronto.ca/services-payments/streets-parking-transportation/transportation-projects/rapidto/rapidto-bus-lanes/eglinton-east-bus-lanes/", target="_blank">City of Toronto</a>. -->
		</p>

	</div>


	<ImageSingle
		imageURL="https://upload.wikimedia.org/wikipedia/commons/0/07/Kingston_Road_in_West_Hill%2C_Scarborough%2C_July_10_2025.jpg"
		caption="Painted bus lanes on Kingston Road in West Hill, Scarborough, July 10, 2025."
		source="Wikimedia Commons."	
		altText=""
		maxWidth="680px"
		link="Yes"
	/>

	<div class="text">

		<p>
			These bus lanes have been shown to improve travel times and reliability for transit users, while also reducing congestion for all road users. They are a clear example of how reallocating space can benefit everyone, not just those who drive. The King Street transit priority corridor showed similar benefits for transit travel times while proposed dedicated transit lanes on Dufferin St. and Bathurst St. south of Bloor St. are estimated to also improve transit travel times. (CLEAN UP PARAGRAPH, ADD LINKS)
		</p>
		<p>
			Toronto has approximately <strong>1,300 kilometres</strong> of highways, major arterial roads, and minor arterial roads. The vast majority of these roads have TTC surface transit routes and have ample space to add dedicated bus or streetcar lanes to speed up these routes. These roads will not truly be effective "arteries" until they are designed to prioritize people who ride public transit, instead of only motor vehicles.
		</p>

	</div>

	<ImageSingle
		imageURL="./images/major-roads-surface-transit-options.png"
		caption=""
		source=""	
		altText=""
		maxWidth="1080px"
		link="No"
	/>

	<div class="text">

		<p>
			Extrapolating from <a href="https://www.toronto.ca/services-payments/streets-parking-transportation/transportation-projects/rapidto/rapidto-bus-lanes/eglinton-east-bus-lanes/", target="_blank">City of Toronto reports of recent costs of bus lanes in Scaroborough</a> (<strong>$470,000 / km</strong>), adding dedicated transit lanes to half of the City's highway and arterial road network would cost approximately <strong>$305 Million</strong>. This is quite low when comparing to <a href="https://schoolofcities.utoronto.ca/wp-content/uploads/2025/04/Understanding-the-Drivers-of-Transit-Construction-Costs-in-Canada_Feb-2025_FINAL.pdf" target="_blank">rising costs of larger public transit infrastructure projects</a> across Canada. 
			For example, the most recent cost estimate for the three-stop Scarborough Subway Extension is <strong>$5.5 Billion</strong> (<strong>$800,000,000 / km</strong>). This is not to say that dedicated surface transit lanes are a replacement for higher capacity public transit projects, but rather that they are a cost-effective way to improve transit service quickly as well as provide connections to potentially all neighbourhoods in city.
		</p>
		<p>	
			To be as successful possible, surface transit routes also require implementing measures like transit-priority signals and enforcement against illegal parking in dedicated transit lanes.
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
			In the core, the costs go beyond opportunity. A University of Toronto report found that illegal on-street parking, including in no-parking zones, or double-parking, “reduces lane capacity and disrupts traffic flow, particularly during peak hours.” Their study found that even relatively short parking violations in the Financial District led to measurable increases in congestion and delays for all road users (UTTRI, 2017).
		</p>
		<!-- https://www.theglobeandmail.com/opinion/editorials/article-the-hidden-costs-of-cheap-parking/ -->

		<p>
			How can on-street parking be converted to better uses? Protected cycling lanes, patios via CafeTO, green space, etc. ___ LANRICK ADD EXAMPLES AND DISCUSS BENEFITS
		</p>
		
		<p>
			<i><b>Add 4 photos here of examples of parking into better uses<br>(1 of a nice protected bike lane, 2 cafeTO, 3 seating/plaza, 4 green buffer or garden)</b></i>
		</p>

		<p>
			What about the costs? Funds from strategies like demand-based parking pricing, increased traffic enforcement, and/or congestion charges could generate ample revenue to re-design Toronto streets.
			Demand-based pricing. LANRICK TO ADD.

			<a href="https://schoolofcities.github.io/king-street-toronto/traffic-violations" target="_blank">Previous School of Cities research found that lack of enforcement on the King Street transit priority corridor</a> is leading to about <strong>$750,000</strong> of lost revenue per day, based on data from the City of Toronto and Toronto Police.

			Similarly, we have <a href="https://schoolofcities.utoronto.ca/could-congestion-pricing-unlock-a-better-toronto/">estimated the potential income of congestion pricing</a>, based on recent travel survey data that a $9 fee for driving into central Toronto would generate over <strong>$2.0 million</strong> per day in revenue. 
		</p>

		<!-- <p>
			One critique on adding cycling infrastructure is that it impacts emergency vehicle access. However, this is not true when designed properly. Data on recent Bloor St. West bike lanes do not show ____
		</p> -->

	</div>


	<div class="text">

		<h3>
			Open streets
		</h3>

		<p>
			What are open streets / pedestrianization of streets - discuss benefits - LANRICK TO ADD TEXT
		</p>

		<p>
			Many cities, e.g. Montreal open dozens of streets for months of the year. Toronto only has Market St (summer), Willcocks St (year round), maybe 1 or 2 more???? and occasional weekend festivals. 
		</p>

		<p>
			<i><b>Add here School of Cities video reel of open street in Calgary design by local school</b></i>
		</p>

		<p>

		</p>

	</div>


	<div class="text">

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
			car={80}
			transit={3}
			walk={15}
			bike={2}
		/>

		<h4>
			Survey of <u>Scarborough</u> residents on which mode should have the "highest priority in terms of space and investment"
		</h4>

		<BarMode
			car={32}
			transit={42}
			walk={19}
			bike={7}
		/>

		<p>
			Moreover, when the City of Toronto proposes new street designs, their survey responses are typically very supportive. <a href="https://www.toronto.ca/legdocs/mmis/2023/te/bgrd/backgroundfile-237354.pdf" target="_blank">85% of survey respondents were "Very Supportive" for pedestrian-only zones in Kensington Market</a>. <a href="https://www.toronto.ca/wp-content/uploads/2025/07/8e69-RapidTO-Bathurst-Consultation-Report.pdf" target="_blank">Nearly 70% of survey respondents agreed that major roads, such as Bathurst Street, should prioritize moving people by public transit</a>, from a recent survey of proposed transit-priority lanes. Even the most politically controversial bike lanes have majority support. For example, <a href="https://www.toronto.ca/wp-content/uploads/2023/05/9871-TTWBloorStW-ConsultationSummaryReport-2023-04-19AODA.pdf" target="_blank">more than 50% of surveyed residents were supportive of bike lanes on Bloor St. West</a> (between Runnymede Road and Resurrection Road).
		</p>

		<p>
			The minority opposition to street re-designs and reduction of parking is sometimes framed around concerns of customer access and deliveries. Deliveries can be adjusted to hours mornings or late at night (e.g. mornings or late at night). While the amount of customers arriving by cars is often over-estimated by merchants. In Toronto, after bike lanes were installed along Bloor St. in the Annex and Koreatown, the percent of visitors who arrived by car did not change significantly. In fact, people were <a href="https://tcat.ca/wp-content/uploads/2019/09/Bike-Lanes-and-Business-on-Bloor-Snapshot-2019-09-04.jpg" target="_blank">spending more</a>.
		</p>

	</div>


	<div class="text">
		
		<h2>
			Political and psychological challenges
		</h2>

		<p>
			So if there is overall support for street re-design projects when they are proposed, and the data of recent projects show little detriment, why are changes limited to a few case studies and sections? Or when changes do happen, why is implementation often riddled with compromises which limit their potential effectiveness?  
		</p>

		<p>	
			Cost should not be a barrier, since as we noted, the cost of prioritizing surface public transit, re-allocating on-street parking, and opening streets is relatively quite small – especially when comparing to major infrastructure projects. Moreover, costs could be covered by more intelligent parking pricing and better enforcement.
		</p>

		<p>
			LANRICK WRITES ABOUT POLITICAL CHALLENGES... CAR BRAIN BIASES... (EDIT ANY TEXT BELOW, CURRENTLY COPY-PASTED BOTH OUR TEXT)
		</p>

		<p>
			A major challenge is shifting from the political status quo, which greatly favours those with access to private motor vehicles and maintains infrastructure that privileges their convenience over equity and community benefit.
		</p>

		<p>
			As John Lorinc writes in Spacing, “Toronto needs to confront the reality that curbside real estate is a limited and highly contested resource. Yet, in many places, we still treat it like an entitlement” (Spacing, 2024). This means space that could otherwise support bike lanes, patios, green buffers, or loading zones is instead handed over, often at low cost, for drivers to leave their cars idle.
		</p>

		<p>
			Policies that reduce car dominance are often perceived as unreasonable, not because of data or evidence, but because of a widespread assumption that driving must remain the default mode of transport. Recent research has framed this as <strong>motonormativity</strong>, which refers to the deep cultural bias that treats car use as normal, necessary, and morally neutral, despite having detrimental safety, equity, and environmental impacts. This bias, shaped by decades of media, built infrastructure, and policy leads many people to apply a different standard of judgment to driving than they would to comparable behaviors. For example, <a href="https://doi.org/10.1504/IJENVH.2023.135446" target="_blank">research in the UK</a>, found that most people opposed exposing others to secondhand smoke, but many accepted toxic car fumes on crowded streets without question. This double standard makes it politically difficult to reallocate road space toward public transit, cycling, and walking even when such changes would improve public health, safety, and sustainability.
		</p>

		<p>
			Similarly, people often over-estimate how many people travel by car, likely because they simply take up more space, which can further skew biases. For example, when bike lanes were being installed on Bloor St in the Annex and Koreatown, <a href="https://tcat.ca/wp-content/uploads/2019/09/Bike-Lanes-and-Business-on-Bloor-Snapshot-2019-09-04.jpg" target="_blank">over half of merchants believed that 25% or more of their customers arrived by car, but the reality was less than 10% on average arrive by car.</a>
		</p>

		<p>
			Another possible barrier to change is <strong>pluralistic ignorance</strong>, a social psychology concept where people individually reject a norm or belief, but incorrectly assume that most others accept it. This can lead to the norm appearing stronger than it actually is. For example, <a href="https://doi.org/10.1016/j.gloenvcha.2025.102980">recent research on motonormativity</a> found that many people assumed that other people’s support for non-car transport was lower than their own support. The positive take of this finding combined with surveys of residents, is that support is there, it just needs to be unlocked with increased research, advocacy, and political will.
		</p>

		
		<!-- https://www.inderscienceonline.com/doi/epdf/10.1504/IJENVH.2023.135446 -->

		<!-- https://www.sciencedirect.com/science/article/pii/S0959378025000172#b0170 -->


	</div>

	<div class="text">

		<h2>
			A fairer future is one we design
		</h2>

		<p>
			Public space belongs to everyone, not just car owners. For too long, Toronto’s streets have served vehicles first. But as we've seen, this is not inevitable. The choice to rebalance our streets is already underway. The successes of CaféTO, the King Street transit corridor, and new protected bike lanes are not isolated experiments; they are a clear verdict. They prove that when we reclaim space from idle cars, we create more room for people, for community, and for a more resilient city.
		</p>
		
		<p>
			The path forward is to make this the rule, not the exception. We can achieve this by implementing smart policies and cost-effective re-designs that treat our land as the valuable public asset it is. This means decisively reallocating on-street parking on streets to create permanent space for wider sidewalks, safer bike lanes, and dedicated surface public transit routes. It means intelligently pricing our curb lanes to manage demand and reinvesting that revenue directly into the neighbourhood improvements residents are asking for: better transit, pedestrian, and cycling infrastructure; and vibrant street-scapes and public spaces. 
		</p>
		
		<p>
			Imagine walking down a curb that is not a lane of cars, but a widened sidewalk filled with planters. Imagine biking on a protected lane unblocked by parked vehicles, or catching a bus that arrives on time because its path is clear.	This isn't a distant dream. When we choose to design streets for people, we build a safer, greener, and more equitable Toronto for everyone, starting with the public space that actually serves all its residents.
		</p>
		
        <!-- <Footnotes footnotes={footnotes} /> -->

		<div class="details">

			<h2>Data & Methods</h2>

			<p>
				Jeff to add detail about the GIS data used for the maps and charts above.
			</p>

		</div>
		
    </div>

	

	<Footer />

</main>


