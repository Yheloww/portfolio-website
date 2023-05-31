
<script>
    import Project from "../../lib/component/project.svelte";
</script>

<div class="wrapper">
    <div class="title">
        <h1 class="very-big">Projects</h1>
        <svg width="100%" height="22" fill="none" xmlns="http://www.w3.org/2000/svg" class="line">
            <path d="M1278 21.5H1288.5V0.5H1278V21.5ZM0 21.5H1278V0.5H0V21.5Z" fill="#FFF176"/>
            </svg>            
    </div>
</div>

<Project/>
<Project/>
<Project/>

<div class="wrapper">
    <div class="title">
        <h1 class="very-big">Dashboards</h1>
        <svg width="100%" height="22" fill="none" xmlns="http://www.w3.org/2000/svg" class="line">
            <path d="M1278 21.5H1288.5V0.5H1278V21.5ZM0 21.5H1278V0.5H0V21.5Z" fill="#FFF176"/>
            </svg>            
    </div>

    <div class=cards>
        <div class="card">
            <h1 class="title-dash">Restaurants</h1>
            <p class="description">Décrire</p>
            <img class="image"src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRe1yI0EHo1qg4pQB-Nt2KX5g3Dr_QkvbWaZQ&usqp=CAU" alt="">
            <button class="site">See dashboard</button>
        </div>
        <div class="card">
            <h1 class="title-dash">Dragonyte</h1>
            <p class="description">Décrire</p>
            <img class="image" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRe1yI0EHo1qg4pQB-Nt2KX5g3Dr_QkvbWaZQ&usqp=CAU" alt="">
            <button class="site">See dashboard</button>
        </div>
    </div>
</div>


<div class="wrapper">
    <div class="title">
        <h1 class="very-big">Visuals</h1>
        <svg width="100%" height="22" fill="none" xmlns="http://www.w3.org/2000/svg" class="line">
            <path d="M1278 21.5H1288.5V0.5H1278V21.5ZM0 21.5H1278V0.5H0V21.5Z" fill="#FFF176"/>
            </svg>            
    </div>
</div>

<div id="curator-feed-default-feed-layout"><a href="https://curator.io" target="_blank" class="crt-logo crt-tag">Powered by Curator.io</a></div>



<style>

h1 {
    margin: 0rem;
}

.title {
    margin-inline: 2rem;
}

.wrapper {
    max-width: 60rem;
    margin-inline: auto;
}

.very-big {
    font-size: 50px;
    font-family: 'Assistant', sans-serif;
    text-transform: uppercase;
    margin-block: 0rem;
}

.card {
    display: flex;
    flex-direction: column;
    background-color: var(--light-blue);
    border-radius: 3rem;
    padding: 2rem;
    gap:2rem;
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
    border-radius: 3rem;
}

.site {
    align-self: center;
}

@media (min-width: 600px) {

    .very-big {
        font-size: 100px;
    }

    .cards{
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        margin-block: 5rem;
    }
}

</style>