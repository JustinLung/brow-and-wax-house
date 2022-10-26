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
		background-image: url('/assets/images/group-photo.jpg');
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

	div:last-child {
		margin-top: 1rem;
	}

	a:first-child {
		background-color: var(--color-white);
		color: var(--color-black);
		font-weight: bold;
		padding: 0.5rem 1rem;
		border-radius: 0.2rem;
	}

	a:last-child {
		background-color: var(--color-black);
		color: var(--color-white);
		font-weight: bold;
		padding: 0.5rem 1rem;
		border-radius: 0.2rem;
	}

	@media (max-width: 55rem) {
		section {
			padding: 0 1rem;
		}

		h1 {
			font-size: 2.5rem;
		}

		p {
			font-size: 1rem;
		}
	}
</style>
