<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=Playfair:wght@500&display=swap" rel="stylesheet">
	<link href="https://fonts.googleapis.com/css2?family=Assistant:wght@500&display=swap" rel="stylesheet">
</svelte:head>


<nav>
	<div class="logo">
		<p>H</p>
	</div>
	<ul class="nav-links">
		<li>
			<a href="/">home</a>
		</li>
		<li>
			<a href="/projects">porfolio</a>
		</li>
		<li>
			<a href="/contact">about me</a>
		</li>
	</ul>
</nav>

<slot/>

<style>
	:root {
		--text-yellow: #FFF176;
		--grey-color: #3E3E3E;
	}

	nav {
		display: flex;
		justify-content:space-between;
		align-items: center;
		background-color: var(--grey-color);
		min-height: 4rem;
		color: var(--text-yellow);
		font-family: 'Assistant', sans-serif;
		padding-left: 1rem;
		padding-right: 4rem;
		font-size: 20px;
		margin-bottom: 0%;
	}

	.logo {
		font-size: 20px;
		margin: 0%;
		padding: 0%;
	}

	.nav-links {
		display: flex;
		width: 40%;
		justify-content: space-between;
		align-items: end;
		justify-self: end;
	}
	.nav-links li{
		list-style: none;
	}

	.nav-links a {
		color: var(--text-yellow);
		text-decoration: none;
		letter-spacing: 2px;
		font-size: 1rem;
	}

</style>