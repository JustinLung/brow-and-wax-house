<section>
	<h2>Services</h2>
	<div>
		<slot />
	</div>
</section>

<style>
	section {
		max-width: 65rem;
		margin: 2rem auto;
		padding: 0 1rem;
	}

	h2 {
		font-size: 2rem;
		margin-bottom: 1rem;
	}

	div {
		display: flex;
		flex-direction: row;
		gap: 1rem;
	}

	@media (max-width: 55rem) {
		div {
			flex-direction: column;
		}
	}
</style>
