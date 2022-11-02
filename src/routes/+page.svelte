<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	// import AboutSection from '$lib/components/indexComponents/AboutSection.svelte';
	import AboutText from '$lib/components/indexComponents/AboutText.svelte';
	import ServiceCard from '$lib/components/indexComponents/ServiceCard.svelte';
	import Services from '$lib/components/indexComponents/Services.svelte';

	const pageTitle = 'Home';
</script>

<svelte:head>
	<title>Brow & Wax House - {pageTitle}</title>
</svelte:head>
<Hero
	heroHeading="Brow & Wax House"
	heroParagraph="For perfect eyebrows and professional hair removal on the body"
/>

<Services>
	<ServiceCard
		serviceLink="/"
		serviceImage="/assets/images/portrait-2.jpg"
		serviceTitle="Brows"
		serviceSubtitle="Eyebrows change the shape of your face. So make sure you have the right one."
	/>
	<ServiceCard
		serviceLink="/"
		serviceImage="/assets/images/portrait-3.jpg"
		serviceTitle="Brows"
		serviceSubtitle="Eyebrows change the shape of your face. So make sure you have the right one."
	/>
</Services>
