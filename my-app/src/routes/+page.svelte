<script>
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
    <div class="principal-section">
        <div class="wrapper">
            <div class="inline-test">
                <h1 class="titre">Hi I'm <span class="yellow-text">Héloïse</span> Feldmann</h1>
                <p class="sous-titre">I'm a junior data 
                    <span class="yellow-text">analyst</span>
                     who likes to create beautiful,<br class="break">
                     <span class="yellow-text">interactive</span> 
                     and thorough stories with 
                     <span class="yellow-text">datas</span>
                </p>
                    <svg width="122" height="122" viewBox="0 0 122 122" fill="none" xmlns="http://www.w3.org/2000/svg" class="round">
                        <circle cx="61" cy="61" r="61" fill="#FFF176"/>
                        <path  class="fleche" d="M58.1115 103.786C59.654 105.368 62.1864 105.4 63.7679 103.857L89.54 78.7215C91.1215 77.179 91.1531 74.6466 89.6107 73.0651C88.0682 71.4836 85.5358 71.4519 83.9543 72.9944L61.0458 95.3372L38.703 72.4287C37.1605 70.8472 34.628 70.8156 33.0465 72.358C31.465 73.9005 31.4334 76.4329 32.9758 78.0144L58.1115 103.786ZM58.0003 18.95L56.9754 100.944L64.9748 101.044L65.9997 19.05L58.0003 18.95Z" fill="#515151"/>
                    </svg>
        </div>
    </div>
</div>

<div class="wrapper">
    <div class="projects-type">
        <ul class="project-list">
            <li>
                <svg width="64" height="64" viewBox="0 0 122 122" fill="none" xmlns="http://www.w3.org/2000/svg" class="bullet">
                    <circle cx="61" cy="61" r="50" fill="#FFF176"/>
                </svg>
                <a href="/projects" class="text-big">Projects</a>
            </li>
            <li>
                <svg width="64" height="64" viewBox="0 0 122 122" fill="none" xmlns="http://www.w3.org/2000/svg" class="bullet">
                    <circle cx="61" cy="61" r="50" fill="#FFF176"/>
                </svg>
                <a href="/projects" class="text-big">Dashboard</a>
            </li>
            <li>
                <svg width="64" height="64" viewBox="0 0 122 122" fill="none" xmlns="http://www.w3.org/2000/svg" class="bullet">
                    <circle cx="61" cy="61" r="50" fill="#FFF176"/>
                </svg>
                <a href="/projects" class="text-big">visuals</a>
            </li>
        </ul>
    </div>
</div>

<div class="wrapper">
    <div class="process" >
        <div transition:fade>
            <h1 class="very-big">process</h1>
            <svg width="100%" height="22" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M1278 21.5H1288.5V0.5H1278V21.5ZM0 21.5H1278V0.5H0V21.5Z" fill="#FFF176"/>
                </svg>            
        </div> 
    
        <div class="cards">
            <div class="card show"><p>Hello</p></div>
            <div class="card show"><p>Hello</p></div>
            <div class="card show"><p>Hello</p></div>
            <div class="card show"><p>Hello</p></div>
        </div>
    </div>
</div>



<style>
    .wrapper {
    max-width: 60rem;
    margin-inline: auto;
    }

    .principal-section {
        margin-top: 0%;
        min-height: 80vh;
        background-color: var(--blue-color);
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 100%;
        overflow: hidden;
        color: white;
        font-family: 'Assistant', sans-serif;
    }

    .titre {
        font-size: 50px;
        line-height: 4rem;
    }

    .sous-titre {
        font-size: 20px;
        line-height: 2rem;
    }
    .yellow-text {
        color: var(--text-yellow);
    }

    .fleche {
        animation: haut-bas 2s infinite linear;
    }

    .projects-type {
        display: flex;
        font-family: 'Assistant', sans-serif;
        font-size: 1rem;
        text-transform: uppercase;
        font-style: bold;
        width: 100%;
        font-size: 30px;
    }

    .inline-test {
        margin-inline: 2rem;
    }

    .round {
        width: max(10%, 5vw);
    }


    .text-big {
        text-decoration: none;
        color: black;
    }

    li:hover {
        opacity: 0.5;
        transition: transform 0.5s ease;

    }
    ul {
        display: flex;
        flex-direction: column; 
    }

    li {
        list-style: none;
        display: flex;
        flex-direction: row;
        justify-content: first baseline;
        align-items: center;
        background-color: var(--blue-color);
        padding: 0.5rem;
        border-radius: 100vw;
        margin-block: 0.5rem;
    }


    @keyframes haut-bas {
        0% {
            transform: translateY(-5px);
        }
        25% {
            transform: translateY(0px)
        }
        50% {
            transform: translateY(5px);
        }
        75% {
            transform: translateY(0px);
        }
        100% {
            transform: translateY(-5px);
        }
    }

    .very-big {
        font-size: 64px;
        font-family: 'Assistant', sans-serif;
        text-transform: uppercase;
        margin-block: 0em;
    }

    .process {
        margin-bottom: 0;
        display: flex;
        flex-direction: column;
        margin-inline: 2rem;
    }

    .cards {
        display: flex;
        flex-direction: column;
        padding: 5%;
        gap: 2rem;
    }
    .card.show {
        color : wheat;
        opacity: 1;
        transition: all 1s ease; 
        transform: translateX(0%);
    }

    .card {
        width:100%;
        background-color: var(--grey-color);
        border-radius: 20px;
        opacity: 0;
        transform: translateX(100%);
    }

    @keyframes slideInFromRight {
    0% {
        transform: translateX(100%);
    }
    100% {
        transform: translateX(0);
    }
    }


    @media (min-width: 600px) {
    .projects-type {
        display: flex;
        font-family: 'Assistant', sans-serif;
        font-size:4vw;
        text-transform: uppercase;
        font-style: bold;
        width: 100%;
        margin-top: 5%;
        margin-bottom: 5%;  
        justify-content: center;
        margin-inline: 0;
    }

    ul {
        display: flex;
        justify-content: center;
        flex-direction: row;
        align-content: center;
        gap: 2rem;
    }

    li {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 1rem;
    }

    .sous-titre {
        font-size: 35px;
        line-height: 2.5rem;
    }

    .very-big {
        font-size: 100px;
    }
    .titre {
        font-size: 64px;
    }
    .bullet {
        width: min(10vh, 5vw);
    }

    .cards {
        flex-direction: row;
    }
}
</style>