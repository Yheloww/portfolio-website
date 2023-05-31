<div class="wrapper">
    <div class="aboutme">
        <div>
            <h1 class="about">ABOUT ME</h1>
            <p class="description">Description</p>
        </div>
        <div>
            <img src="./image/heloise.jpg" alt="héloïse">
        </div>
    </div>

    <div class="cards">
        <div class="card" id="progra-card">
            <h1>PROGRAMMING</h1>
            <ul class=progra-list>
                <li>
                    <p>Python</p>
                </li>
                <li>
                    <p>Javascript</p>
                </li>
                <li>
                    <p>SQL</p>
                </li>
                <li>
                    <p>html</p>
                </li>
            </ul>
        </div>

        <div class="card" id="tool-card">
            <h1>TOOLS</h1>
            <ul class=tool-list>
                <li>
                    <p>Power BI</p>
                </li>
                <li>
                    <p>Tableau</p>
                </li>
                <li>
                    <p>Adobe illustrator</p>
                </li>
                <li>
                    <p>Touch Designer</p>
                </li>
            </ul>
        </div>
    </div>
</div>

<style>
    .wrapper {
    max-width: 60rem;
    margin-inline: auto;
    }

    .aboutme {
    max-width: 60rem;
    display: grid;
    margin-inline: 2rem;
    font-family: 'Assistant', sans-serif;
    margin-block: 5rem;
    }


img {
    max-width: 100%;  
    object-fit: cover;
    border-radius: 3rem;
}

    @media (min-width: 600px) {
    .aboutme{
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        margin-block: 10rem;
        }
    }

</style>