<script>
    let {currentPage = $bindable()} = $props();
</script>
{#if currentPage == "blog" || currentPage == "home"}
<div class="blog-container">
    <div class="blog-card item1">
        <h1>Headless Content Management System (CMS) Exploration</h1>
        <p>&emsp; For an assignment, I chose Ghost as the headless CMS because it is easier to work with compared 
            to some alternatives I’ve tried, like Strapi. Its Markdown editor and user-friendly API make content 
            creation and integration a straightforward process, especially when using SvelteKit, which I found 
            surprisingly easy to work with. While Ghost is primarily designed for blogs, this specialization 
            actually simplifies my work, as it comes with native support for tagging and content categorization, 
            both of which are ideal for organizing blog posts. The learning curve is manageable, and I don’t 
            have to navigate SQL database issues like I did with Strapi, allowing me to focus on improving 
            styling and functionality rather than troubleshooting database management. Overall, Ghost meets 
            the projects needs well.</p>
        <button class="readmore-btn">READ MORE</button>
    </div>
    <div class="blog-card">
        <h1>Title</h1>
        <p>Excerpt</p>
        <button class="readmore-btn">READ MORE</button>
    </div>
    <div class="blog-card">
        <h1>Title</h1>
        <p>Excerpt</p>
        <button class="readmore-btn">READ MORE</button>
    </div>
    <div class="blog-card item1">
        <h1>Title</h1>
        <p>Excerpt</p>
        <button class="readmore-btn">READ MORE</button>
    </div>
</div>
{/if}
<style>
    .blog-container {
        margin: 0;
        padding: 0;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 1rem;
        /* padding: 1rem; */
        margin: auto;
        margin-left: 1.25rem;
        margin-right: 1.25rem;
        justify-content: center;
    }
    .item1 {
        grid-column: auto / span 2;
    }
    .blog-card {
        background-color: white;
        padding: 1rem;
        border-radius: 2rem;
        font-family: "Crimson Text", serif;
        color: #434343;
    }
    .readmore-btn {
        color: #ffffff;
        background-color: #FF9176;
        border: none;
        cursor: pointer;
        width: 15rem;
        padding: 0.25rem;
        padding-right: 1.5rem;
        padding-left: 1.5rem;
        border-radius: 15rem;
        font-family: monospace;
        font-size: 1.5rem;
        margin-top: 0.5rem;
        transition: 200ms;
    }
    .readmore-btn:hover {
        background-color: rgb(230, 114, 84);
        filter: drop-shadow(0.3rem 0.3rem #00000040)
    }
</style>