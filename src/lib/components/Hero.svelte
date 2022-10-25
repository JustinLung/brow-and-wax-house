<script lang="ts">
	export let heroTitle: string;
	export let heroSubtitle: string;
</script>

<section>
	<h1>{heroTitle}</h1>
	<p>{heroSubtitle}</p>
	<div>
		<a href="/services">Our Services</a>
		<a
			href="https://browandwaxhouse.salonware.nl/"
			rel="noreferrer"
			target="_blank"
			sveltekit:prefetch>Book Apointment</a
		>
	</div>
</section>

<style>
	section {
		background-image: url('/assets/images/model.png'),
			linear-gradient(42deg, var(--color-cream) 34%, var(--color-purple) 74%);
		background-size: cover;
		background-position: center;
		height: 80vh;
		padding: 0 3rem;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	h1 {
		font-size: 3rem;
	}

	p {
		font-size: 1.3rem;
		max-width: 30rem;
	}

	div {
		margin-top: 1rem;
	}

	a:first-child {
		background-color: var(--color-pink);
		color: var(--color-black);
		font-weight: bold;
		padding: 0.5rem 1rem;
		border-radius: 0.2rem;
		border: 2px solid var(--color-pink);
		transition: 0.2s ease-in;
	}

	a:last-child {
		background-color: var(--color-purple);
		color: var(--color-white);
		font-weight: bold;
		padding: 0.5rem 1rem;
		border-radius: 0.2rem;
		border: 1px solid var(--color-purple);
		transition: 0.2s ease-in;
	}

	@media (max-width: 55rem) {
		section {
			padding: 0 1rem;
		}
	}
</style>
