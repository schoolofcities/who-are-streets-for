<script>
	export let id;
	let footnoteId = `footnote-${id}`;
	let refId = `footnote-ref-${id}`;
</script>

<span class="footnote-ref-wrapper">
	<a id={refId} href={`#${footnoteId}`} class="footnote-ref" on:click|preventDefault={() => {
		const element = document.getElementById(footnoteId);
		if (element) element.scrollIntoView({ behavior: 'auto', block: 'start' });
	}}>
		{id}
	</a>
</span>

<style>
	.footnote-ref-wrapper {
		position: relative;
		font-size: 1em;
		line-height: 1;
		display: inline-block;
	}
	.footnote-ref {
		vertical-align: super;
		font-size: 0.8em;
		font-family: SourceSerifBold;
		font-weight: normal;
		margin-left: 0;
		margin-right: 0.1em; /* slight breathing room after */
		text-decoration: none;
		color: var(--brandPink);
		white-space: nowrap;
	}
	.footnote-ref:hover {
		color: var(--brandLightBlue);
	}
</style>
