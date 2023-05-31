


<div class="wrapper">
    <div class="project">
        <div class="image">
            <img src="https://dynaimage.cdn.cnn.com/cnn/c_fill,g_auto,w_1200,h_675,ar_16:9/https%3A%2F%2Fcdn.cnn.com%2Fcnnnext%2Fdam%2Fassets%2F220818142713-dogs-tears-emotions-wellness-stock.jpg" alt="corgi" >
        </div>
        <div class="text">
            <h1>Project name</h1>
            <p>Et omnis nulla est maxime omnis id quia consequatur qui cupiditate repellat qui dolore quia non harum deserunt. Non laudantium expedita eum architecto perspiciatis ab quas quis cum quibusdam culpa sit repudiandae voluptates aut reiciendis excepturi! Est culpa ipsa non soluta omnis est quam saepe et sequi magnam ut officia voluptas. Qui repellendus perferendis qui internos suscipit in eius praesentium et voluptas harum?</p>
            <div class="button">
                <button class="github">github</button>
                <button class="site">website</button>
                <button class="about">about</button>
            </div>
        </div>
    </div>
</div>


<style>
h1 {
    margin: 0rem;
}

.wrapper {
    max-width: 60rem;
    margin-inline: auto;
}

.image img {
    width: 100%;
    height: 100%;
    border-radius: 3rem;
}

img {
    max-width: 100%;  
    object-fit: cover;
}

.project {
    max-width: 60rem;
    display: grid;
    margin-inline: 2rem;
    font-family: 'Assistant', sans-serif;
    margin-block: 5rem;
}

.text {
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

@media (min-width: 600px) {
    .project{
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        margin-block: 10rem;
    }
}


</style>