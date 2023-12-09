<script>
	import Header from "./Header.svelte";
	import Footer from "./Footer.svelte";
	import "./styles.css";
	export const prerender = true;
</script>

<div class="background"></div>
<Header />
<div class="body">
	<main>
		<slot />
	</main>
	<!-- <Three /> -->
</div>

<Footer />

<style>
	.body {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		width: 21cm; /* A4 width */
		margin: auto;
		z-index: -10;
		overflow: hidden;
	}
	.background {
		margin: 0;
		top: 0;
		left: 0;
		position: fixed;
		background: url(images/blueprint.jpeg) repeat;
		background-repeat: repeat;
		background-size: 50%;
		z-index: -10;
		width: 100vw;
		height: 100vh;
		overflow: hidden;
	}
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		max-width: 64rem;
	}
</style>
