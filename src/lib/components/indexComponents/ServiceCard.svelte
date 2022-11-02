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
		<a href="/{serviceLink}">Read more</a>
	</div>
</article>

<style>
	article {
		background-color: var(--color-light-cream);
		width: 100%;
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
		padding: 1rem 3rem 2rem;
	}

	h3 {
		font-size: var(--font-size-md);
		font-weight: 600;
		margin-bottom: 0.5rem;
	}

	p {
		font-size: var(--font-size-normal);
		line-height: 1.5rem;
		margin-bottom: 1rem;
		max-width: 25rem;
	}

	a {
		background-color: var(--color-black);
		color: var(--color-white);
		padding: 0.5rem 1.5rem;
		border-radius: 0.5rem;
		transition: 0.3s ease-in-out;
		border: 1px solid var(--color-black);
		font-weight: 300;
	}

	a:hover {
		background-color: transparent;
		border: 1px solid var(--color-black);
		color: var(--color-black);
	}
</style>
