
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
            <button class="site"><a href="https://app.powerbi.com/links/q5BKyyUa-J?ctid=bf6256d9-2940-465b-bd70-1b366185f183&pbi_source=linkShare&bookmarkGuid=07f97c7e-a254-43fd-9d9f-5be34c7b0a21">See dashboard</a></button>
        </div>
        <div class="card show">
            <h1 class="title-dash">Dragonyte</h1>
            <p class="description">This tableau dashboard is the result of a use case proposed by accenture during my becode training. It analyze the datas of Dragonyte brewery a fake clientThen we cleaned and analyze the datas to get some insights out. At the end was a presentation of our findings to accenture people.</p>
            <img class="image" src="./image/dragonite.png" alt="tableau dashboard">
            <button class="site"><a href="https://public.tableau.com/app/profile/h.lo.se.feldmann/viz/StoryDragonyte/Histoire1">See dashboard</a></button>
        </div>
    </div>
</div>

</div>

<div class="border">

<div class="wrapper">
    <div class="title">
        <h1 class="big">Visuals</h1> 
        <p class="description"> This part is more artistic I recently started to document my learning of a great tool called touch designer. It is used a lot in new media art field. When I wil get a better understanding of the software, I want to merge my knowledge of data viz with this software. you can follow my journey on instagram. </p>          
        <a href="https://www.instagram.com/helow_exp_/"><svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 50 50" width="50px" height="50px">    
            <path d="M 16 3 C 8.83 3 3 8.83 3 16 L 3 34 C 3 41.17 8.83 47 16 47 L 34 47 C 41.17 47 47 41.17 47 34 L 47 16 C 47 8.83 41.17 3 34 3 L 16 3 z M 37 11 C 38.1 11 39 11.9 39 13 C 39 14.1 38.1 15 37 15 C 35.9 15 35 14.1 35 13 C 35 11.9 35.9 11 37 11 z M 25 14 C 31.07 14 36 18.93 36 25 C 36 31.07 31.07 36 25 36 C 18.93 36 14 31.07 14 25 C 14 18.93 18.93 14 25 14 z M 25 16 C 20.04 16 16 20.04 16 25 C 16 29.96 20.04 34 25 34 C 29.96 34 34 29.96 34 25 C 34 20.04 29.96 16 25 16 z"/></svg>
        </a>
        </div>
    <div class="media">
        <img class="visuals" src="./image/test.jpg" alt="">
        <img class="visuals" src="./image/test2.jpg" alt="">
        <img class="visuals" src="./image/test3.jpg" alt="">
    </div>
</div>




</div>

<style>

.visuals {
    background-size: cover;
    aspect-ratio: 1/1;
    margin-block: 1rem
}

p {
    font-size: 20px;
}
h1 {
    margin: 0rem;
}
.media {
    display: grid;
    margin-inline: 2rem;
}

.title {
    margin-inline: 2rem;
    font-family: 'Assistant', sans-serif;

}
.border {
    border: 0.5px solid #dddddd;
    margin-inline: 1rem;
    border-radius: 1rem;
    background-color: white;
    margin-bottom: 4rem;
}
.wrapper {
    max-width: 75rem;
    margin-inline: auto;
}

a {
    text-decoration: none;
    color: black;
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
    background-color: whitesmoke;
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
    border: 0.7px solid var(--text-yellow);
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
    .media {
        grid-template-columns: 1fr 1fr 1fr;
        gap: 1rem;
        margin-block: 2rem;
    }
}

</style>