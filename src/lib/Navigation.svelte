<script>
	import { Svg } from '$lib';

	let menuOpen = false;

	function toggleMenu() {
		menuOpen = !menuOpen;
	}
</script>

<header>
	<nav>
		<ul>
			<li><Svg name="hva-fdnd" /></li>
			<li><button id="menu-btn" on:click={toggleMenu}>MENU</button></li>
		</ul>
		<ul id="menu-content" class:menu-open={menuOpen}>
			<li>Home</li>
			<li>We Love Webs</li>
			<li>FDND Agency</li>
			<li>Archief</li>
			<li><a href="#">Contact</a></li>
		</ul>
	</nav>
</header>

<style>
	header {
		position: relative;
		padding-top: 1rem;
		margin-bottom: -1px;
	}
	

	header nav {
		width: 100%;

		@media (min-width: 768px) {
			display: flex;
			justify-content: center;
			align-items: center;
		}
	}

	header nav ul:nth-child(1) {
		list-style-type: none;
		display: flex;
		justify-content: space-between;
		align-items: center;

		@media (min-width: 768px) {
			margin: 0 3rem 0 0;
		}
	}

	header nav ul:nth-child(1) li:nth-child(2) {
		z-index: 5;
		
		@media (min-width: 768px) {
			display: none;
		}
	}

	header nav ul:nth-child(1) button::before {
		content: '';
		z-index: -1;
		position: absolute;
		width: 100%;
		height: 100%;
		border: 1px solid var(--blue);
		background-color: var(--green);
		border-radius: 10px;
		right: 2px;
		top: 2px;
	}

	header nav ul:nth-child(1) button {
		position: relative;
		border: 1px solid var(--blue);
		padding: 0.5rem 1rem;
		background-color: var(--green);
		border-radius: 10px;
		color: var(--blue);
		font-weight: 700;
		text-decoration: none;
		cursor: pointer;
	}

	header nav ul:nth-child(1) button:hover {
		right: 1px;
		top: 1px;
	}

	header nav ul:nth-child(1) button:hover::before {
		right: 1px;
		top: 1px;
	}

	header nav ul:nth-child(1) button:active {
		right: 2px;
		top: 2px;
	}

	header nav ul:nth-child(1) button:active::before {
		right: 1px;
		top: 1px;
	}

	header nav ul:nth-child(2) {
		padding: 3rem 0;
		width: 100%;
		height: 100vh;
		background-color: #000000aa;
		position: absolute;
		top: 0;
		right: -100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-around;
		transition: 450ms cubic-bezier(0, 0.62, 0.57, 1.02);
		z-index: 2;

		@media (min-width: 768px) {
			border-radius: 2rem 2rem 0 0;
			background-color: var(--white);
			position: relative;
			top: auto;
			right: auto;
			flex-direction: row;
			height: 80%;
			padding: 2rem 0;
			font-size: 1rem;
		}
	}

	header nav ul:nth-child(2)::before {
		content: '';
		position: absolute;
		left: 0rem;
		bottom: 1px;
		transform: translateX(-100%);
		width: var(--radius);
		height: var(--radius);
		background: radial-gradient(circle at left top, transparent 1.48rem, var(--white) 1.48rem) border-box;
	}

	header nav ul:nth-child(2).menu-open {
		right: 0;
	}

	header nav ul:nth-child(2) li {
		color: #fff;
		transition: 300ms;
		list-style-type: none;

		@media (min-width: 768px) {
			color: var(--blue);
		}
	}
	
	header nav ul:nth-child(2) li a {
		color: #fff;
		transition: 300ms;
		text-decoration: none;

		@media (min-width: 768px) {
			color: var(--blue);
			border: 3px solid var(--blue);
			border-radius: .5rem;
			padding: .5rem 1rem;
		}
	}


</style>
