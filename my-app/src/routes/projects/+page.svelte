


<div class="wrapper">
    <div class="title">
        <h1 class="very-big">Projects</h1>
        <svg width="100%" height="22" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1278 21.5H1288.5V0.5H1278V21.5ZM0 21.5H1278V0.5H0V21.5Z" fill="#FFF176"/>
            </svg>            
    </div>
</div>

<div class="wrapper">
    <div class="project">
        <div class="image">
            <img src="https://dynaimage.cdn.cnn.com/cnn/c_fill,g_auto,w_1200,h_675,ar_16:9/https%3A%2F%2Fcdn.cnn.com%2Fcnnnext%2Fdam%2Fassets%2F220818142713-dogs-tears-emotions-wellness-stock.jpg" alt="corgi" >
        </div>
        <div class="text">
            <h1>Project name</h1>
            <p>Et omnis nulla est maxime omnis id quia consequatur qui cupiditate repellat qui dolore quia non harum deserunt. Non laudantium expedita eum architecto perspiciatis ab quas quis cum quibusdam culpa sit repudiandae voluptates aut reiciendis excepturi! Est culpa ipsa non soluta omnis est quam saepe et sequi magnam ut officia voluptas. Qui repellendus perferendis qui internos suscipit in eius praesentium et voluptas harum?</p>
            <button class="github">github</button>
            <button class="site">website</button>
            <button class="about">about</button>
        </div>
    </div>
</div>




<style>
img {
    max-width: 100%;
}
.title {
    margin-inline: 2rem;
}

.wrapper {
    max-width: 45rem;
    margin-inline: auto;
}

.image {
    border: 2px solid red
}

.project {
    max-width: 46rem;
    display: grid;
    margin-inline: 2rem;
}
.very-big {
    font-size: 64px;
    font-family: 'Assistant', sans-serif;
    text-transform: uppercase;
    margin-block: 0rem;
}

@media (min-width: 600px) {
    .project{
        grid-template-columns: 1fr 1fr;
        gap: 2rem;
    }
    .very-big {
        font-size: 100px;
    }
}

</style>