
<script>
    import Project from "../../lib/component/project.svelte";
    import { fade, fly } from "svelte/transition";
    import { onMount } from "svelte";

    onMount(()=> {
        const cards = document.querySelectorAll(".card")

        const observer = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                entry.target.classList.toggle("show", entry.isIntersecting)
            })
        }, {
            threshold:1,
        })

    cards.forEach(card => {
            observer.observe(card)
        })

    })

</script>

<div class="wrapper">
    <h1 class="very-big">PORTFOLIO</h1>
</div>
<div class="border first">

<div class="wrapper">
    <div class="title">
        <h1 class="big">Projects</h1>          
    </div>
</div>

<Project/>
<Project/>
<Project/>

</div>

<div class=border>

<div class="wrapper">
    <div class="title">
        <h1 class="big">Dashboards</h1>
    </div>


    <div class=cards>
        <div class="card show">
            <h1 class="title-dash">Restaurants</h1>
            <p class="description">Décrire</p>
            <img class="image"src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRe1yI0EHo1qg4pQB-Nt2KX5g3Dr_QkvbWaZQ&usqp=CAU" alt="">
            <button class="site">See dashboard</button>
        </div>
        <div class="card show">
            <h1 class="title-dash">Dragonyte</h1>
            <p class="description">Décrire</p>
            <img class="image" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRe1yI0EHo1qg4pQB-Nt2KX5g3Dr_QkvbWaZQ&usqp=CAU" alt="">
            <button class="site">See dashboard</button>
        </div>
    </div>
</div>

</div>

<div class="border">

<div class="wrapper">
    <div class="title">
        <h1 class="big">Visuals</h1>           
    </div>
</div>

<div id="curator-feed-default-feed-layout"><a href="https://curator.io" target="_blank" class="crt-logo crt-tag">Powered by Curator.io</a></div>

</div>

<style>

h1 {
    margin: 0rem;
}

.title {
    margin-inline: 2rem;
}
.border {
    border-top: 4px solid var(--text-yellow);
}
.wrapper {
    max-width: 60rem;
    margin-inline: auto;
}

.big {
    font-size: 30px;
    font-family: 'Assistant', sans-serif;
    text-transform: uppercase;
    margin-block: 0rem;
    margin-top: 2rem;
}

.very-big {
    font-size: 50px;
    font-family: 'Assistant', sans-serif;
    text-transform: uppercase;
    margin-block: 2rem;
    margin-inline: 2rem;
}

.card {
    display: flex;
    flex-direction: column;
    border : 0.5px solid #bcbcbc;
    border-radius: 1rem;
    padding: 2rem;
    gap:2rem;
    opacity: 0;
}

.card.show{
    opacity: 1;
    transition: all 1s ease;
}


.card:hover {
    background-color: #dddddd;
}

.cards {
    max-width: 60rem;
    display: grid;
    margin-inline: 2rem;
    font-family: 'Assistant', sans-serif;
    margin-block: 3rem;
    gap: 2rem;
}

img {
    max-width: 100%;  
    object-fit: cover;
    border-radius: 1rem;
}

.site {
    align-self: center;
}

@media (min-width: 600px) {

    .very-big {
        font-size: 100px;
    }

    .big {
        font-size: 50px;
    }

    .cards{
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        margin-block: 5rem;
    }
}

</style>