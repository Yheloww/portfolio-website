<script>
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

  import { base } from "$app/paths";
</script>

<div class="video-wrapper">
  <video muted playsinline autoplay loop disablepictureinpicture>
    <source src="./test.webm" type="video/webm" />
    Your browser does not support the video tag.
  </video>
  <div class="principal-section">
    <div class="wrapper">
      <div class="inline-test">
        <h1 class="titre">
          Hi I'm <span class="yellow-text">Héloïse</span> Feldmann
        </h1>
        <p class="sous-titre">
          I'm a junior data
          <span class="yellow-text">analyst</span>
          who likes to create beautiful,<br class="break" />
          <span class="yellow-text">interactive</span>
          and thorough stories with
          <span class="yellow-text">datas</span>
        </p>
        <svg
          width="53"
          height="55"
          viewBox="0 0 60 70"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            class="fleche"
            d="M23.879 59.4374C25.2287 60.8212 27.4446 60.8489 28.8284 59.4992L51.3789 37.5055C52.7627 36.1559 52.7904 33.94 51.4408 32.5562C50.0911 31.1723 47.8752 31.1447 46.4914 32.4943L26.4465 52.0443L6.89654 31.9994C5.54689 30.6155 3.33099 30.5878 1.94718 31.9375C0.563365 33.2871 0.535666 35.503 1.88531 36.8869L23.879 59.4374ZM23.5945 0.18245L22.8849 56.9499L29.8844 57.0374L30.594 0.269943L23.5945 0.18245Z"
            fill="#FFF176"
          />
        </svg>
      </div>
    </div>
  </div>
</div>

<div class="wrapper">
  <div class="projects-type">
    <ul class="project-list">
      <li>
        <a href="{base}/projects" class="text-big button">Projects</a>
      </li>
      <li>
        <a href="{base}/projects.html#dashboard" class="text-big button">Dashboard</a
        >
      </li>
      <li>
        <a href="{base}/projects.html#visuals" class="text-big button">visuals</a>
      </li>
    </ul>
  </div>
</div>
<div class="border">
  <div class="wrapper">
    <div class="process">
      <div transition:fade>
        <h2 class="very-big">process</h2>
      </div>

      <div class="cards">
        <div class="card show">
          <h1>CLEAN</h1>
          <p class="content">
            To clean my data I can use different tools depending on the data. I
            can clean with <b>python</b> to have very good and thorough
            cleaning. But I also use <b>Power bi</b>to have fast results. I also
            recently started to use <b>Observable</b> notebooks to make projects
          </p>
        </div>
        <div class="card show">
          <h1>ASK</h1>
          <p class="content">
            After cleaning the data, I spend lots of times asking <b
              >questions</b
            >
            to the data. That's the phase that helps me get a <b>direction</b> for
            my vizualisations and my findings. I try to ask a lot of questions to
            be able to wrap my head around the data..
          </p>
        </div>
        <div class="card show">
          <h1>IDEATE</h1>
          <p class="content">
            I start creating some raw visualization and some wireframe. I like
            give attention to the <b>visual presentation</b>, it's a great phase
            to put things on <b>paper</b> and <b>organize</b> everything.
          </p>
        </div>
        <div class="card show">
          <h1>VIZUALIZE</h1>
          <p class="content">
            to visualize the findings I use a different range of tools, I can
            make a <b>dashboards</b> using power bi or Tableau. But I am also
            starting to make <b>visual experience</b> on the web by presenting
            the data story using some <b>frontend</b> skills and data viz libraries
          </p>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .content {
    padding: 1rem;
    font-size: 20px;
  }

  h1 {
    text-align: center;
  }

  video {
    object-fit: cover;
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    z-index: -100;
  }
  .video-wrapper {
    min-height: 500px;
    position: relative;
    overflow: hidden;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-inline: 1rem;
    border-radius: 1rem;
    z-index: -100;
  }

  .wrapper {
    max-width: 100rem;
    margin-inline: auto;
  }

  .border {
    border: 0.5px solid #dddddd;
    margin-inline: 1rem;
    border-radius: 1rem;
    background-color: rgb(32, 32, 32);
    padding-block: 2rem;
  }

  .principal-section {
    min-height: 80vh;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-family: "Assistant", sans-serif;
    margin-inline: 1rem;
    border-radius: 1rem;
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
    font-family: "Assistant", sans-serif;
    font-size: 1rem;
    text-transform: uppercase;
    font-style: bold;
    font-size: 30px;
    justify-content: center;
  }

  .inline-test {
    margin-inline: 2rem;
  }

  .text-big {
    text-decoration: none;
    color: black;
    font-size: 2rem;
  }

  li:hover {
    opacity: 0.5;
    transition: all 1s ease;
    background-color: var(--text-yellow);
    color: black;
  }
  ul {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    align-items: center;
    padding-left: 0%;
  }

  li {
    list-style: none;
    display: flex;
    flex-direction: row;
    background-color: white;
    border-radius: 1rem;
    border: 0.5px solid #dddddd;
    padding: 1rem;
  }

  @keyframes haut-bas {
    0% {
      transform: translateY(-5px);
    }
    25% {
      transform: translateY(0px);
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
    font-family: "Assistant", sans-serif;
    text-transform: uppercase;
    margin-block: 0em;
    color: white;
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
    gap: 2rem;
  }
  .card.show {
    color: black;
    opacity: 1;
    transition: all 1s ease;
  }

  .card {
    width: 100%;
    background-color: whitesmoke;
    opacity: 0;
    padding: 0.5rem;
    border-radius: 1rem;
    border: 0.5px solid #dddddd;
    font-family: "Assistant", sans-serif;
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
      font-family: "Assistant", sans-serif;
      font-size: 4vw;
      text-transform: uppercase;
      font-style: bold;
      margin-top: 5%;
      margin-bottom: 5%;
      margin-inline: 0;
      justify-content: space-around;
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

    .cards {
      flex-direction: row;
    }
  }
</style>
