<script lang="ts">
	export let serviceTitle: string;
	export let serviceSubtitle: string;
	export let serviceImage: string;
	export let serviceLink: string;
</script>

<article>
	<div>
		<img src={serviceImage} alt={serviceTitle} />
	</div>
	<div>
		<h3>{serviceTitle}</h3>
		<p>{serviceSubtitle}</p>
		<a href="/{serviceLink}">Prices</a>
	</div>
</article>

<style>
	article {
		background-color: var(--color-cream);
		width: 30rem;
		border-radius: 0.5rem;
	}

	img {
		width: 100%;
		border-top-left-radius: 0.5rem;
		border-top-right-radius: 0.5rem;
	}

	div:first-child {
		height: 20rem;
	}

	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: top center;
	}

	div:last-child {
		padding: 1rem 1rem 2rem;
	}

	h3 {
		font-size: 1.5rem;
	}

	p {
		font-size: 1rem;
		margin-bottom: 1rem;
	}

	a {
		background-color: var(--color-black);
		color: var(--color-white);
		padding: 0.5rem 1.5rem;
		border-radius: 0.5rem;
		transition: 0.3s ease-in-out;
	}

	a:hover {
		background-color: var(--color-white);
		color: var(--color-black);
	}

	@media (max-width: 55rem) {
		article {
			width: 100%;
		}
	}
</style>
