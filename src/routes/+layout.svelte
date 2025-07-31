<script>
    import Works from '$lib/pages/works/+page.svelte'
    import About from '$lib/pages/about/+page.svelte'

    let currentPage = $state("home")
</script>
<div class="main-container">
    <nav class="navbar">
        <h1>IBRAHIM SHEHADEH</h1>
        <span></span>
        <div class="nav-btns">
            <button class={currentPage == "home" ? "nav-btn btn-active" : "nav-btn btn-inactive"} onclick={() => {currentPage = "home"}}>HOME</button>
            <button class={currentPage == "work" ? "nav-btn btn-active" : "nav-btn btn-inactive"} onclick={() => {currentPage = "work"}}>WORK</button>
            <button class={currentPage == "projects" ? "nav-btn btn-active" : "nav-btn btn-inactive"} onclick={() => {currentPage = "projects"}}>PROJECTS</button>
            <!-- <button class={currentPage == "blog" ? "nav-btn btn-active" : "nav-btn btn-inactive"} onclick={() => {currentPage = "blog"}}>BLOG</button> -->
            <button class={currentPage == "about" ? "nav-btn btn-active" : "nav-btn btn-inactive"} onclick={() => {currentPage = "about"}}>About</button>
        </div>
    </nav>
    <div class="section2">
        <h2>A <strong>DEVELOPER</strong> WHO ENJOYS SOLVING REAL PROBLEMS WITH CLEAN, THOUGHTFUL CODE.</h2>
        <div class="contact-container">
            <p class="contact-title">Let’s get in touch!</p>
            <p class="contact-p">If you’re into building useful tools with good people, add me to your roster.</p>
            <button class="contact-btn">CONTACT</button>
        </div>
    </div>
    <Works bind:currentPage={currentPage}/>
    <About bind:currentPage={currentPage}/>
</div>


<style>
    .main-container {
        width: 100%;
        overflow: hidden;
    }
    .navbar {
        width: 100%;
        display: grid;
        justify-content: center;
        position: relative;
    }
    .navbar h1 {
        width: fit-content;
        text-align: center;
        background-color: #ffffff;
        padding: 0.5rem;
        padding-right: 8rem;
        padding-left: 8rem;
        font-family: monospace;
        font-size: 3rem;
        color: #FF9176;
        border: 0.2rem solid #434343;
        border-radius: 15rem;
        margin: auto;
        margin-top: 1.875rem;
        z-index: 1;
    }
    .navbar span {
        width: 100vw;
        max-width: 100%;
        position: relative;
        top: -2.55rem;
        left: 0;
        border-top: 0.2rem solid #434343;
        z-index: 0;
    }
    .nav-btns {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0;
        margin: auto;
    }
    .nav-btn {
        margin: 0.5rem;
        padding: 0.25rem;
        padding-right: 1.5rem;
        padding-left: 1.5rem;
        
        border-radius: 15rem;
        font-family: monospace;
        font-size: 1.75rem;
        transition: 200ms;
        
    }
    .btn-active {
        background-color: #434343;
        border: 0.2rem solid #ffffff;
        color: #FF9176;
        cursor: default;
    }
    .btn-inactive {
        color: #F0B4A5;
        cursor: pointer;
        background-color: #ffffff;
        border: 0.2rem solid #ffffff;
    }
    .btn-inactive:hover {
        color: #FF9176;
        background-color: #ebebeb;
        border: 0.2rem solid #ebebeb;
        filter: drop-shadow(0.3rem 0.3rem #00000040)
    }
    .section2 {
        margin-left: 1.25rem;
        margin-right: 1.25rem;
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: #434343;
    }
    .section2 h2 {
        width: 50%;
        font-family: "Crimson Text", serif;
        font-weight: 400;
        font-size: 2.2vw;
    }
    .contact-container {
        width: 30rem;
        display: grid;
        background-color: white;
        padding: 1rem;
        border-radius: 2rem;
        color: #FF9176;
    }
    .contact-title {
        font-family: monospace;
        font-size: 1.5rem;
        font-weight: 700;
        margin: 0;
    }
    .contact-p {
        font-family: monospace;
        font-size: 1rem;
        margin: 0;
    }
    .contact-btn {
        color: #ffffff;
        background-color: #FF9176;
        border: none;
        cursor: pointer;
        width: 10rem;
        padding: 0.25rem;
        padding-right: 1.5rem;
        padding-left: 1.5rem;
        border-radius: 15rem;
        font-family: monospace;
        font-size: 1.5rem;
        margin-top: 0.5rem;
        transition: 200ms;
    }
    .contact-btn:hover {
        background-color: rgb(230, 114, 84);
        filter: drop-shadow(0.3rem 0.3rem #00000040)
    }
</style>