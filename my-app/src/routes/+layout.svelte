<script>
	import { fly,fade } from 'svelte/transition';
	import { page } from '$app/stores';
	import Transition from '../lib/component/Transition.svelte'
	import Footer from '../lib/component/Footer.svelte';
	export let data;
	let height =0;
	let width = 0;
	let clicked = false;
	import { base } from "$app/paths";

	</script>


<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=Playfair:wght@500&display=swap" rel="stylesheet">
	<link href="https://fonts.googleapis.com/css2?family=Assistant:wght@500&display=swap" rel="stylesheet">
</svelte:head>



<svelte:window bind:innerHeight={height} bind:innerWidth={width}/>

<nav class="flex">
	<div class="logo">
		<a href="{base}/">H</a>
	</div>


	{#if width < 500 }
	<svg class:active={clicked} on:click={ () => clicked = !clicked} on:keypress={ () => clicked = !clicked} class="menu" width="29" height="23" viewBox="0 0 29 23" fill="none" xmlns="http://www.w3.org/2000/svg">
		{#if !clicked}
		<rect width="29" height="3" rx="1.5" fill="black"/>
		<rect y="10" width="29" height="3" rx="1.5" fill="black"/>
		<rect y="20" width="29" height="3" rx="1.5" fill="black"/>
		{:else}
		<path fill-rule="evenodd" clip-rule="evenodd" d="M4.26105 1.13123C3.63629 0.506468 2.62335 0.506468 1.99859 1.13123C1.37383 1.75599 1.37383 2.76893 1.99859 3.39369L9.62989 11.025C10.0204 11.4155 10.0204 12.0487 9.62989 12.4392L1.13117 20.9379C0.506408 21.5627 0.506408 22.5756 1.13117 23.2004C1.75593 23.8251 2.76887 23.8251 3.39363 23.2004L11.8924 14.7017C12.2829 14.3111 12.916 14.3111 13.3066 14.7017L21.6066 23.0017C22.2313 23.6264 23.2443 23.6264 23.869 23.0017C24.4938 22.3769 24.4938 21.364 23.869 20.7392L15.569 12.4392C15.1785 12.0487 15.1785 11.4155 15.569 11.025L23.0016 3.59241C23.6264 2.96765 23.6264 1.95471 23.0016 1.32995C22.3768 0.705187 21.3639 0.705188 20.7391 1.32995L13.3066 8.76253C12.916 9.15305 12.2829 9.15305 11.8924 8.76253L4.26105 1.13123Z" fill="white" class="croix"/>
		{/if}
	</svg>
		{#if clicked}
		<ul class="nav-links flex" transition:fly="{{ x:300, duration: 800}}" >
			<li>
				<a on:click={ () => clicked = !clicked} href="{base}/">home</a>
			</li>
			<li>
				<a on:click={ () => clicked = !clicked} href="{base}/projects">porfolio</a>
			</li>
			<li>
				<a on:click={ () => clicked = !clicked} href="{base}/contact">about me</a>
			</li>
		</ul>
		{/if}
	{:else}
	<ul class="big-links flex">
		<li>
			<a href="{base}/">home</a>
		</li>
		<li>
			<a href="{base}/projects">porfolio</a>
		</li>
		<li>
			<a href="{base}/contact">about me</a>
		</li>
	</ul>
	{/if}
</nav>

{#key data.pathname}
<div in:fly={{ y: -50, duration: 300, delay:350}}
	out:fly={{ y:-50, duration: 300}}>
    <slot/>
</div>
{/key}

<Footer/>


<style>
	.croix:hover {
	fill: var(--text-yellow);
}
	:root {
		--text-yellow: #FFF176;
		--grey-color: #3E3E3E;
		--blue-color: #6D9BB3;
		--light-blue: #8FD9FF;
		--white-color: #ffff;
	}

	nav {
		/* background-color: var(--blue-color); */
		color: black;
		font-family: 'Assistant', sans-serif;
		align-items: center;
		justify-content: space-between;
		padding: 1rem;
		border: 0.5px solid #dddddd;
		margin: 1rem;
		border-radius: 1rem;
		background-color: white;
	}

	.logo a {
		margin: 2rem;
		text-decoration: none;
		color: black;
		font-size: 2rem;
		margin-block: 0rem;
	}

	.big-links {
		list-style: none;
		margin: 0;
		padding: 0;
		text-decoration: none;

	}

	.big-links a {
		color: black;
		text-decoration: none;
		
	}

	.flex {
		display: flex;
		gap: 2rem;
	}

	.nav-links {
		gap : 2.5em;
		margin: 0;
		padding: 0;
		position: fixed;
		inset: 0 0 0 40%;
		background-color: hsla(0, 0%, 0%, 0.7);
		backdrop-filter: blur(0.5rem);

		flex-direction: column;
		padding: min(20vh,7rem) 2rem;
		list-style: none;
		border-top-left-radius: 1rem;
		border-bottom-left-radius: 1rem;
		border: 0.2px solid rgb(119, 119, 119);

	}

	.nav-links a {
		color: rgb(249, 249, 249);
		text-decoration: none;
		text-transform: uppercase;
	}
	
	.menu {
		z-index: 200;
	}

	a:hover {
		color: var(--text-yellow)
	}


</style>