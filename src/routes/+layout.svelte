<script lang="ts">
	import '../styles/global.css';
	import '../styles/theme.css';
	import Header from '$lib/components/Header.svelte';
</script>

<Header />
<main>
	<slot />
</main>
