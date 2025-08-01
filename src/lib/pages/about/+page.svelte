<script>
    let {currentPage = $bindable()} = $props();
    import logosImg from '$lib/imgs/logos.svg';
    import ibrahimHeadshot from '$lib/imgs/ibrahimshehadeh_headshot.png';
</script>
{#if currentPage == "home" || currentPage == "about"}
<div class="section1">
    <img class="headshot" src={ibrahimHeadshot} />
    <h1>Ibrahim Shehadeh</h1>
    <h2>I <strong>BUILD</strong> TOOLS FOR <strong>BUSINESSES, PRODUCTION TEAMS, AND MUNICIPALITIES</strong>
        USING SVELTE, REACT, NODE, AND POSTGRESQL - AND HELPED CUT <strong>COSTS</strong>, 
        SPEED THINGS UP, AND <strong>MAKE LIFE EASIER</strong> FOR THE PEOPLE USING THEM.</h2>
    <button class="about-btn">DOWNLOAD RESUME</button>
    <!-- <img src={logosImg} class="logos"/> -->
</div>
<div class="section2">
    <p><strong>Languages & Skills:</strong> JavaScript, TypeScript, HTML, CSS, SCSS, TailwindCSS, C#, Dart</p>
    <p><strong>Frameworks & Libraries:</strong> Svelte, React, Next.js, Express.js, .NET, Bootstrap, Panellum</p>
    <p><strong>Databases:</strong> MongoDB, PostgreSQL, Neon, Local Storage</p>
    <p><strong>APIs & Web Technologies:</strong> RESTful APIs, JSON, HTTP, the DOM, Browser Compatibility</p>
    <p><strong>DevOps:</strong> AWS (S3, Lambda, EC2, API Gateway), Vercel, Netlify, GitHub Actions (CI/CD)</p>
    <p><strong>Tools & Platforms:</strong> Git, Figma, Illustrator, Lucidchart, Postman, Linux</p>
    <p><strong>Soft Skills:</strong> Cross-functional collaboration, Leadership & Training, Client Communication, Time Management, 
        Debugging & Troubleshooting</p>
    
</div>
{/if}
<style>
    .section1 {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: auto;
        align-items: center;
        padding: 1vw;
        margin: auto;
        /* width: 70vw; */
        color: #ff9176;
    }
    .headshot {
        width: 30vw;
        background-color: #ffffff;
        padding: 1vw;
        /* border: 1rem solid white; */
        border-radius: 30vw;
        grid-column: 1;
        grid-row: 1 / span 2;
        justify-self: end;
    }
    .section1 h1 {
        align-self: end;
        margin: 0;
        margin-right: auto;
        font-family: "Crimson Text", serif;
        font-weight: 800;
        font-size: 3vw;
        background-color: #ffffff;
        padding: 1rem 1rem 0 1rem;
        border-radius: 1rem 1rem 0 0;
    }
    .section1 h2 {
        background-color: #ffffff;
        padding: 1rem 1rem 1rem 1rem;
        border-radius: 0 1rem 1rem 1rem;
        margin: 0;
        align-self: start;
        font-family: "Crimson Text", serif;
        font-weight: 400;
        font-size: 1.5vw;
        grid-row: 2;
    }
    .section1 h1, h2, button {
        grid-column: 2;
    }
    .section1 button {
        grid-row: 2;
    }
    .logos {
        grid-row: 2;
        grid-column: 2;
        width: 20rem;
        margin-top: 6rem;
        justify-self: flex-end;
        align-self: flex-end;
        background-color: #ffffff;
        border-radius: 0 1rem 1rem 1rem;
    }
    .about-btn {
        color: #ffffff;
        background-color: #FF9176;
        border: none;
        cursor: pointer;
        width: 20vw;
        padding: 0.25rem;
        padding-right: 1.5vw;
        padding-left: 1.5vw;
        border-radius: 15rem;
        font-family: monospace;
        font-size: 1.5vw;
        margin-left: 1rem;
        transition: 200ms;
        align-self: flex-end;
        margin-bottom: 7vw;
    }
    .about-btn:hover {
        background-color: rgb(230, 114, 84);
        filter: drop-shadow(0.3rem 0.3rem #00000040)
    }
    .section2 {
        color: #434343;
        display: grid;
        grid-template-rows: auto;
        justify-content: center;
        padding: 1vw;
        align-items: center;
        width: 60vw;
        margin: auto;
    }
    .section2 p {
        /* width: 50%; */
        font-family: "Crimson Text", serif;
        font-weight: 400;
        font-size: 2.5vw;
        grid-column: 1;
        margin: 0;
    }
    .section2 strong {
         font-family: "Crimson Text", serif;
        font-size: 3vw;
        font-weight: 700;
    }
    @media screen and (max-width: 768px) {
        .headshot{
            width: 90%;
        }
        .section1 {
            grid-template-rows: auto auto auto;
        }
        .section1 h1 {
            width: 100%;
            font-size: 5vw
        }
        .section1 h2 {
            width: 100%;
            font-size: 3vw;
            border-radius: 0 0 1rem 1rem;
        }
        .about-btn {
            grid-row: 3;
            margin-bottom: 0;
        }
    }
    @media screen and (min-width: 769px) {
        .about-btn {
            margin-bottom: 7vw;
        }
        .headshot{
            width: 100%;
        }
    }
    @media screen and (min-width: 1200px) {
        .about-btn {
            margin-bottom: 7vw;
        }
    }
</style>