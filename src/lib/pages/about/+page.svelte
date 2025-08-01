<script>
    let {currentPage = $bindable()} = $props();
    import logosImg from '$lib/imgs/logos.svg';
    import ibrahimHeadshot from '$lib/imgs/ibrahimshehadeh_headshot.png';
    import resume from '$lib/resume/IbrahimShehadeh.pdf'
</script>
{#if currentPage == "home" || currentPage == "about"}
<div class="section1">
    <img class="headshot" src={ibrahimHeadshot} />
    <div class="about-grid">
        <h1>Ibrahim Shehadeh</h1>
        <h2>I <strong>BUILD</strong> TOOLS FOR <strong>BUSINESSES, PRODUCTION TEAMS, AND MUNICIPALITIES</strong>
            USING SVELTE, REACT, NODE, AND POSTGRESQL - AND HELPED CUT <strong>COSTS</strong>, 
            SPEED THINGS UP, AND <strong>MAKE LIFE EASIER</strong> FOR THE PEOPLE USING THEM.</h2>
        <div class="about-btn-container">
            <button class="about-btn" onclick={() => {window.open(resume)}}>DOWNLOAD RESUME</button>
        </div>
    </div>
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
        /* display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: auto; */
        display: flex;
        align-items: center;
        padding: 1vw;
        gap: 1vw;
        margin: auto;
        /* width: 70vw; */
        color: #ff9176;
    }
    .headshot {
        max-width: 50%;
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
        padding: 2vw 2vw 0 2vw;
        border-radius: 2vw 2vw 0 0;
    }
    .section1 h2 {
        background-color: #ffffff;
        padding: 1rem;
        border-radius: 0 2vw 2vw 0;
        margin: 0;
        align-self: start;
        font-family: "Crimson Text", serif;
        font-weight: 400;
        font-size: 1.5vw;
        grid-row: 2;
    }
    .about-grid {
        display: grid;
        grid-row: 2;
    }
    .about-btn-container {
        background-color: #ffffff;
        width: fit-content;
        padding: 2vw;
        border-radius: 0 0 2vw 2vw;
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
        font-size: 2vw;
        transition: 200ms;
        align-self: flex-end;
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
        padding: 4vw;
        align-items: center;
        width: fit-content;
        margin: auto;
        margin-bottom: 10vw;
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
        .section1 h1 {
            font-size: 3.4vw
        }
        .section1 h2 {
            font-size: 3vw;
        }
    }
    @media screen and (min-width: 769px) {

    }
    @media screen and (min-width: 1200px) {
    }
</style>