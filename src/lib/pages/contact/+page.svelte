<script>
    let {currentPage = $bindable()} = $props();
</script>
<div class="contact-container">
    <h1>Lets get it <strong>DONE</strong>.</h1>
    <h2>Email:</h2>
    <p>ibrahim16shehadeh@gmail.com</p>
    <h2 id="linkedIn">LinkedIn:</h2>
    <a href="https://www.linkedin.com/in/ibrahim-khalil-shehadeh/">linkedin.com/in/ibrahim-khalil-shehadeh/</a>
</div>
<style>
    .contact-container {
        display: grid;
        grid-template-columns: 16vw auto;
        width: fit-content;
        justify-content: center;
        align-items: center;
        margin: auto;
        padding: 2vw;
        color: #FF9176;
        font-family: monospace;
    }
    .contact-container h1 {
        text-align: center;
        width: 100%;
        font-size: 3vw;
        font-weight: 400;
        background-color: #ffffff;
        border-radius: 2vw 2vw 0 0;
        
        margin: 0;
        padding: 2vw;
    }
    .contact-container h2 {
        grid-column: 1;
        text-align: right;
        font-size: 2vw;
        font-weight: 400;
        background-color: #ffffff;
        padding: 2vw;
        margin: 0;
    }
    #linkedIn {
        border-radius: 0 0 0 2rem;
    }
    .contact-container p, a {
        font-size: 2vw;
        font-weight: 400;
        background-color: #ffffff;
        
        padding: 2vw;
        margin: 0;
    }
    .contact-container p {
        border-radius: 0 2vw 0 0;
    }
    .contact-container a {
        color:#2d77d8;
        text-decoration: none;
        border-radius: 0 0 2vw 0;
    }
    .contact-container a:hover {
        color:#1d4c89;
        text-decoration: wavy;
    }
    @media screen and (max-width: 768px) {
        .contact-container h1 {
            font-size: 0.6rem;
        }
        .contact-container h2{
            font-size: 0.6rem;
        }
        .contact-container p {
            font-size: 0.6rem;
        }
        .contact-container a {
            font-size: 0.6rem;
        }

    }
</style>