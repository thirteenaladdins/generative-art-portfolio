<!-- <script>
    import CustomLink from '../components/CustomLink.svelte';
</script> -->

<!-- add this later -->
<!-- <CustomLink/> -->

<div class="container">
    <h1>migfrig</h1>
    <a class="link-item" href="https://www.instagram.com/migfrig/">Instagram</a>
    <!-- <a href="/Gallery">Gallery</a> -->
    <a class="link-item" href="https://editor.p5js.org/thirteenaladdins/sketches/">Generative Art</a>

    <a class="link-item" href="https://github.com/thirteenaladdins">Github</a>
    <!-- <a href="/Shop">Shop</a> -->
</div>
    
<style>
    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 100vh;
        font-family: Arial, Helvetica, sans-serif;
    }

    /* style with material style button */
    .link-item {
        display: inline-block;
        padding: 0.5rem 1rem;
        margin: 0.5rem;
        text-decoration: none;
        color: #fff;
        background-color: #000;
        border-radius: 0.25rem;
        transition: all 0.2s ease;
        font-family: Arial, Helvetica, sans-serif;
        font-weight: bold;
        width: 10rem;
    }

    a:hover {
        color: #000;
        background-color: #fff;
    }

    a:focus {
        text-decoration: none;
        color: inherit;
        font-size: 1rem;
        font-family: Arial, Helvetica, sans-serif;
        padding: 0.125rem;
    }

</style>