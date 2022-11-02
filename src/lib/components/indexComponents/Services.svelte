<section>
	<h2>Services</h2>
	<div>
		<slot />
	</div>
</section>

<style>
	section {
		margin-top: 5rem;
		padding: 0 7rem;
	}

	h2 {
		font-size: 2rem;
		margin-bottom: 1.5rem;
		position: relative;
	}

	h2:after {
		content: '';
		height: 3.5rem;
		width: 3.5rem;
		left: 7rem;
		z-index: -1;
		top: 50%;
		transform: translateY(-50%);
		position: absolute;
		background-color: var(--color-cream);
		border-radius: 50%;
	}

	div {
		display: flex;
		flex-direction: row;
		gap: 2.5rem;
	}

	@media (max-width: 55rem) {
		section {
			padding: 1rem;
			margin-top: 1rem;
		}
		div {
			flex-direction: column;
		}
	}
</style>
