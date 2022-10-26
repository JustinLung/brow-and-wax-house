<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import ServiceCard from '$lib/components/indexComponents/ServiceCard.svelte';
	import Services from '$lib/components/indexComponents/Services.svelte';
</script>

<Hero
	heroTitle="Brow & Wax House"
	heroSubtitle="For perfect eyebrows and professional hair removal on the body"
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
