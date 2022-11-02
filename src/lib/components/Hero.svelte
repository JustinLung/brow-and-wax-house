<script lang="ts">
	export let heroHeading: string;
	export let heroParagraph: string;
</script>

<section class="hero">
	<div class="hero__content-left">
		<h1 class="hero__content-left__heading">{heroHeading}</h1>
		<p class="hero__content-left__paragraph">{heroParagraph}</p>
		<div class="hero__content-left__links">
			<a href="/" class="hero__content-left__links-link">Our Services</a>
			<a href="/" class="hero__content-left__links-link">Book Appointment</a>
		</div>
		<ul class="hero__content-left__list">
			<li><a href="/">Instagram</a></li>
			<li>&#183;</li>
			<li><a href="/">Facebook</a></li>
		</ul>
	</div>
	<div class="hero__content-right">
		<figure class="hero__content-right__image-container">
			<img
				src="/assets/images/group-photo.jpg"
				alt="Group"
				class="hero__content-right__image-container__image"
			/>
		</figure>
	</div>
</section>

<style>
	.hero {
		padding: 0 7rem;
		margin: 5rem auto 0;
		display: flex;
		flex-direction: row;
		gap: 2rem;
	}

	.hero__content-left,
	.hero__content-right {
		display: flex;
		flex-direction: column;
		justify-content: center;
		flex: 1;
	}

	.hero__content-left__heading {
		font-size: var(--font-size-2xl);
	}

	.hero__content-left__list {
		list-style: none;
		padding: 0;
		font-weight: 500;
		display: flex;
		flex-direction: row;
		gap: 1rem;
	}

	.hero__content-left__list a {
		color: var(--color-black);
	}

	.hero__content-left__paragraph {
		font-size: var(--font-size-sm);
		line-height: 1.5rem;
		max-width: 25rem;
	}

	.hero__content-left__links {
		margin: 1rem 0;
	}

	.hero__content-left__links-link {
		padding: 0.5rem 1rem;
		border-radius: 0.2rem;
		border: 1px solid var(--color-black);
		transition: 0.3s ease;
	}

	.hero__content-left__links-link:first-child {
		background-color: var(--color-black);
		color: var(--color-white);
	}

	.hero__content-left__links-link:first-child:hover {
		background-color: transparent;
		color: var(--color-black);
	}

	.hero__content-left__links-link:last-child {
		background-color: transparent;
		color: var(--color-black);
	}

	.hero__content-left__links-link:last-child:hover {
		background-color: var(--color-black);
		color: var(--color-white);
	}

	.hero__content-right__image-container {
		margin: 0;
		padding: 1rem;
		width: 100%;
		background-color: var(--color-cream);
		border-radius: 0.5rem;
	}

	.hero__content-right__image-container__image {
		border-radius: 0.2rem;
		width: 100%;
	}

	@media (max-width: 72rem) {
		.hero__content-left__heading {
			font-size: var(--font-size-xl);
		}
	}

	@media (max-width: 60rem) {
		.hero {
			padding: 1rem;
			flex-direction: column;
			gap: 1rem;
		}

		.hero__content-left__heading {
			font-size: var(--font-size-lg);
		}

		.hero__content-left__paragraph {
			font-size: var(--font-size-normal);
		}
	}
</style>
