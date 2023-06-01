
<script>
    import Project from "../../lib/component/project.svelte";
    import { fade, fly } from "svelte/transition";
    import { onMount } from "svelte";

    // onMount(()=> {
    //     const cards = document.querySelectorAll(".card")

    //     const observer = new IntersectionObserver(entries => {
    //         entries.forEach(entry => {
    //             entry.target.classList.toggle("show", entry.isIntersecting)
    //         })
    //     }, {
    //         threshold:1,
    //     })

    // cards.forEach(card => {
    //         observer.observe(card)
    //     })

    // })

    let link = "https://yheloww.github.io/remakeHackaton/"

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

<Project web_link={link} 
         github_link={"https://github.com/Yheloww/remakeHackaton"}
         title={"Education for climate"}
         description={"scrolly telling web experience about the education for climate in belgium. Project made during the scrolly telling hackaton organised by rtbf. In collaboration with 3 other people from different background. This version is the polished version that i made to exercise my fronted and data viz skills."}
         picture={"./image/hackaton.png"}
         />

<Project web_link={link} 
        github_link={"https://github.com/Yheloww/remakeHackaton"}
        title={"D3 project"}
        description={"scrolly telling web experience about the education for climate in belgium. Project made during the scrolly telling hackaton organised by rtbf. In collaboration with 3 other people from different background. This version is the polished version that i made to exercise my fronted and data viz skills."}
        picture={"./image/hackaton.png"}
        />
         
<Project web_link={"https://prediction-mhn8.onrender.com/"} 
        github_link={"https://github.com/Yheloww/real-estate-price-prediction"}
        title={"real estate prediction"}
        description={"Little application based on a machine learning algorithm. It predicts the potential price of your real estate by you entering some charachteristics"}
        picture={"./image/predictor.png"}
        />

</div>

<div class=border>

<div class="wrapper">
    <div class="title">
        <h1 class="big">Dashboards</h1>
    </div>


    <div class=cards>
        <div class="card show">
            <h1 class="title-dash">Restaurants</h1>
            <p class="description">This power bi dashboard is meant for people to find restaurants for their next trip in Europe. It has been thought as a survey and you can explore the various aspects of it as the price range the city where you want to go, the best ranked restaurants and so on ...</p>
            <img class="image"src="./image/restaurant.png" alt="predictor">
            <button class="site">See dashboard</button>
        </div>
        <div class="card show">
            <h1 class="title-dash">Dragonyte</h1>
            <p class="description">This tableau dashboard is the result of a use case proposed by accenture during my becode training. It analyze the datas of Dragonyte brewery a fake clientThen we cleaned and analyze the datas to get some insights out. At the end was a presentation of our findings to accenture people.</p>
            <img class="image" src="./image/dragonite.png" alt="tableau dashboard">
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

p {
    font-size: 20px;
}
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
    justify-content: space-between;
}

.card.show{
    opacity: 1;
    transition: all 1s ease-in;
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

button {
    border-radius: 0.5rem;
    border: 0.7px solid #a5a5a5;
    background-color: #dddddd;
    margin-bottom: 0;
    padding: 0.5rem;
    font-family: 'Assistant', sans-serif;
    font-size: 20px;   
}

button:hover {
    background-color: var(--text-yellow);
    transition: all 0.5s ease;
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