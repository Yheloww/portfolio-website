<svelte:head>
    
</svelte:head>


<nav>
		<p>H</p>
		<a href="/">home</a>
		<a href="/projects">porfolio</a>
		<a href="/contact">about me</a>
</nav>

<slot/>

<style>
	p {
		color: #FFF176;
		font-size: 2rem;
		margin: 0%;
		flex-basis: 50%;
		justify-self: left;
	}
	a {
		text-decoration: none;
		color: #FFF176;
		font-size: 1.2rem;
		font-family: Arial, Helvetica, sans-serif;
		flex-basis: 11%;
	}
	a:hover {
		color:orange;
	}

	nav {
		background-color: #3E3E3E;
		padding: 1rem;
		margin: none;
		display: flex;
		gap: 5rem;
		justify-content: end;
		margin: 0rem 0rem 0rem 0rem;
		align-items: center;

	}

</style>