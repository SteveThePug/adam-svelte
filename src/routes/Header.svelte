<script>
	import { page } from "$app/stores";
</script>

<header>
	<a href="./" class="header-link">Adam</a>
</header>

<style>
	header {
		height: 5vh;
		width: 100vw;
		display: flex;
		justify-content: space-between;
		align-items: center;
		overflow: hidden;
	}
	.header-link {
		color: white;
		padding: 10px;
		flex: 1;
		text-align: left;
	}

	@keyframes moveLeft {
		0% {
			transform: translateX(-25%);
		}
		50% {
			transform: translateX(25%);
		}
		100% {
			transform: translateX(-25%);
		}
	}

	.header-link {
		font-size: 3vh;
		font-variation-settings: "ELSH" 1;
		font-variation-settings: "ELSH" 2;
		font-variation-settings: "wght" 400;
		align-self: center;
		text-align: center;
	}
	.header-link:hover {
		text-decoration: none;
		font-variation-settings: "ELSH" 15;
		font-variation-settings: "ELSH" 45;
		font-variation-settings: "wght" 800;
	}
</style>
