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
    <h1 class="titre principal">Hi I'm <span class="yellow-text">Héloïse</span> Feldmann</h1>
    <p class="sous-titre principal">I'm a junior data 
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

<div class="projects-type">
    <ul>
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

<footer class="footer">
</footer>


<style>

    .principal-section {
        margin-top: 0%;
        min-height: 80vh;
        background-color: var(--grey-color);
        display: flex;
        flex-direction: column;
        justify-content: center;
        line-height: 4rem;
        width: 100%;
        overflow: hidden;
    }
    .principal {
        margin-left: 15%;
        color: white;
        font-family: 'Assistant', sans-serif;
        margin-right: 10%;
    }

    .titre {
        font-size: 64px;
    }

    .sous-titre {
        font-size: 40px;
    }
    .yellow-text {
        background-color: var(--text-yellow);
        color: var(--grey-color);
        border-radius: 10px;  
    }

    .round {
        margin-left: 15%;
        margin-top: 2.5%;
    }

    .fleche {
        animation: haut-bas 2s infinite linear;
    }

    .projects-type {
        display: flex;
        font-family: 'Assistant', sans-serif;
        font-size:40px;
        text-transform: uppercase;
        font-style: bold;
        width: 100%;
        margin-top: 5%;
        margin-bottom: 5%;
        
    }

    .text-big {
        text-decoration: none;
        color: black;
    }

    li:hover {
        transform: translateY(-10px);
        transition: transform 0.5s ease;
    }

    ul {
        display: flex;
        align-items: start;
        justify-content: space-evenly;
        width: 100%;
        list-style: none;
    }
    li {
        display: flex;
        align-items: center;
        justify-content: left;
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
        font-size: 100px;
        font-family: 'Assistant', sans-serif;
        text-transform: uppercase;
        margin-block: 0em;
    }

    .process {
        margin-left: 5%;
        margin-bottom: 0;
        display: flex;
        flex-direction: column;
    }

    .cards {
        display: flex;
        flex-direction: row;
        padding: 5%;
        gap: 5%;
        justify-content: space-between;
        align-items: center;
    }
    .card.show {
        color : wheat;
        opacity: 1; 
    }

    .card {
        width:100%;
        height: 40vh;
        background-color: var(--grey-color);
        flex-basis: 25%;
        border-radius: 20px;
        opacity: 0;
    }

    @keyframes slideInFromRight {
    0% {
        transform: translateX(100%);
    }
    100% {
        transform: translateX(0);
    }
    }

  


    footer {
        height: 150px;
        width: 100%;
        background-color: var(--grey-color);
    }
</style>