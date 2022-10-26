<script lang="ts">
	let isActive = false;

	function toggleNavMenu() {
		isActive = !isActive;

		isActive ? document.body.classList.add('freeze') : document.body.classList.remove('freeze');
	}
	function closeNavMenu() {
		isActive = false;
		document.body.classList.remove('freeze');
	}
</script>

<header>
	<img src="/assets/images/logo.png" alt="logo" />
	<nav class:active={isActive}>
		<a href="/" sveltekit:prefetch on:click={closeNavMenu}>Home</a>
		<a href="/" sveltekit:prefetch on:click={closeNavMenu}>Services</a>
		<a href="/" sveltekit:prefetch on:click={closeNavMenu}>About</a>
		<a href="/" sveltekit:prefetch on:click={closeNavMenu}>Contact</a>
		<a
			href="https://browandwaxhouse.salonware.nl/"
			rel="noreferrer"
			target="_blank"
			sveltekit:prefetch
			on:click={closeNavMenu}>Book Appointment</a
		>
	</nav>
	<button on:click={toggleNavMenu} class:active={isActive}>
		<span />
		<span />
		<span />
	</button>
</header>

<style>
	header {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 1rem;
	}

	img {
		position: relative;
		max-width: 15rem;
		z-index: 99;
	}

	nav {
		display: none;
		flex-grow: 1;
	}

	nav a {
		position: relative;
		color: var(--color-black);
	}

	nav.active {
		position: fixed;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		font-size: 1.3rem;
		font-weight: bold;
		gap: 0.8rem;
		inset: 0;
		width: 100%;
		height: 100vh;
		overflow: hidden;
		z-index: 20;
		background-color: var(--color-white);
	}

	nav.active a {
		filter: brightness(85%);
		width: 85%;
		padding: 0.5rem;
	}

	button {
		all: unset;
		display: block;
		position: relative;
		z-index: 1;
		cursor: pointer;
		z-index: 30;
	}

	button span {
		display: block;
		width: 2rem;
		height: 0.2rem;
		margin-bottom: 5px;
		position: relative;
		background-color: var(--color-black);
		border-radius: 6px;
		transform-origin: 0 0;
		transition: 0.4s;
	}

	button span:last-child {
		margin: 0;
	}

	button.active span:nth-child(1) {
		transform: translate(0px, -2px) rotate(45deg);
	}

	button.active span:nth-child(2) {
		opacity: 0;
		transform: translateX(15px);
	}

	button.active span:nth-child(3) {
		transform: translate(-3px, 3px) rotate(-45deg);
	}

	@media (min-width: 60rem) {
		header {
			padding: 1rem 3rem;
		}

		nav {
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			gap: 1rem;
			position: relative;
			height: auto;
		}

		button {
			display: none;
		}

		nav a::before {
			display: block;
		}

		nav a:first-child {
			margin-left: auto;
		}

		nav a:last-child {
			background-color: var(--color-black);
			color: var(--color-white);
			font-weight: bold;
			padding: 0.5rem 1rem;
			border-radius: 0.2rem;
			border: 1px solid var(--color-purple);
			transition: 0.2s ease-in;
			margin-left: auto;
		}

		nav a:last-child:hover {
			background-color: transparent;
			color: var(--color-purple);
			border: 1px solid var(--color-purple);
			padding: 0.5rem 1rem;
			border-radius: 0.2rem;
		}
	}
</style>
