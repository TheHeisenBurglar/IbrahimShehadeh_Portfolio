<script>
    let {currentPage = $bindable()} = $props();
    import ims2Img from '$lib/imgs/ims2.jpg';
    import ims1Img from '$lib/imgs/ims1.jpg';
    import hamiltonImg from '$lib/imgs/hamilton.jpg';
    import uxbridgeImg from '$lib/imgs/uxbridge.jpg';
    import ajaxImg from '$lib/imgs/ajax.jpg';
    import northwoodImg from '$lib/imgs/northwood.jpg';

    import kittingtimerImg from '$lib/imgs/kittingtimer.jpg';
    import pixelheartImg from '$lib/imgs/pixelheart.jpg';
</script>
<div class="works-container">
    <div class={currentPage == "home" ? "works-card item1" : currentPage == "work" ? "works-card item1" : "hidden"}>
        <img src={hamiltonImg} />
        <h1>Hamilton Tour - Render Developments</h1>
        <p>As my first project at Render Developments—and as a new Hamilton resident—this tour was a meaningful starting point.</p>
    </div>
    <div class={currentPage == "home" ? "works-card" : currentPage == "work" ? "works-card" : "hidden"}>
        <img src={uxbridgeImg} />
        <h1>Uxbridge Tour - Render Developments</h1>
        <p>Designed and built from scratch using the Pannellum JavaScript library, HTML, and CSS.</p>
    </div>
    <div class={currentPage == "home" ? "works-card" : currentPage == "work" ? "works-card" : "hidden"}>
        <img src={ajaxImg} />
        <h1>Ajax Tour - Render Developments</h1>
        <p>This project marked a new direction for both myself and Render Developments.</p>
    </div>
    <div class={currentPage == "home" ? "works-card" : currentPage == "work" ? "works-card" : "hidden"}>
        <img src={northwoodImg} />
        <h1>Northwood Tour - Render Developments</h1>
        <p>In this project, I took a more focused approach, refining specific elements rather than overhauling the entire experience.</p>
    </div>
    <div class={currentPage == "home" ? "works-card" : currentPage == "work" ? "works-card" : "hidden"}>
        <img src={ims2Img} />
        <h1>Inventory Management System V2</h1>
        <p>This was a complete redesign of the original inventory management system, and the first project I was formally contracted to develop.</p>
    </div>
    <div class={currentPage == "home" ? "works-card" : currentPage == "work" ? "works-card" : "hidden"}>
        <img src={ims1Img} />
        <h1>Inventory Management System V1</h1>
        <p>My first full-stack application deployed for daily use by multiple users across departments.</p>
    </div>

    <div class={currentPage == "home" ? "works-card" : currentPage == "projects" ? "works-card" : "hidden"}>
        <img src={kittingtimerImg} />
        <h1>Kitting Timer - DCM</h1>
        <p>This project was born out of a desire to expand my web development skills through practical problem-solving.</p>
    </div>
    <div class={currentPage == "home" ? "works-card" : currentPage == "projects" ? "works-card" : "hidden"}>
        <img src={pixelheartImg} />
        <h1>PixelHert - IT EXPO</h1>
        <p>As the lead front-end developer for Pixelheart, I designed and prototyped a responsive user interface, ensuring a consistent and intuitive experience across mobile and desktop devices.</p>
    </div>
</div>
<style>
    .works-container {
        margin: 0;
        padding: 0;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 1rem;
        /* padding: 1rem; */
        margin: auto;
        margin-left: 1.25rem;
        margin-right: 1.25rem;
        justify-content: center;
    }
    .works-card {
        display: grid;
        text-align: left;
    }
    .works-card h1, p  {
        padding: 0;
        margin: 0;
        margin-left: 1rem;
        font-family: "Crimson Text", serif;
        color: #434343;
    }
    .works-card h1 {
        font-weight: 700;
        font-size: 1.3rem;
        /* letter-spacing: 0.1rem; */
    }
     .works-card p {
        font-weight: 400;
        font-size: 1rem;
     }
    .works-card img {
        box-sizing: border-box;
        position: relative;
        padding: 1rem;
        width: 100%;
        height: 20rem;
        object-fit: cover;
        object-position: top left;
        transition: 200ms;
        border-radius: 1.5rem;
    }
    .works-card img:hover {
        padding-right: 0.25rem;
        padding-top: 0.25rem;
        padding-left: 0.75rem;
        padding-bottom: 0.75rem;
        border-top-right-radius: 0.75rem;
        cursor: pointer;
        filter: drop-shadow(-0.5rem 0.5rem #ffffff)
    }

    /* Manual grid positioning */
    .item1 {
        grid-column: 1 / span 2;
    }
    .hidden {
        display: none;
    }
</style>