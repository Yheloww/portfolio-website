
<script>
    import Project from "../../lib/component/project.svelte";
</script>

<div class="wrapper">
    <div class="title">
        <h1 class="very-big">Projects</h1>
        <svg width="100%" height="22" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1278 21.5H1288.5V0.5H1278V21.5ZM0 21.5H1278V0.5H0V21.5Z" fill="#FFF176"/>
            </svg>            
    </div>
</div>

<Project/>
<Project/>
<Project/>
<Project/>



<style>
h1 {
    margin: 0rem;
}

.title {
    margin-inline: 2rem;
}

.wrapper {
    max-width: 45rem;
    margin-inline: auto;
}

.very-big {
    font-size: 64px;
    font-family: 'Assistant', sans-serif;
    text-transform: uppercase;
    margin-block: 0rem;
}

@media (min-width: 600px) {

    .very-big {
        font-size: 100px;
    }
}

</style>