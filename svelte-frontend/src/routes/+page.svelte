<script>
    import { Router, Route } from "svelte-routing";
    import NavBar from "../components/NavBar.svelte";

    // export let url = "";
</script>
  
<style>
     h1 {
        font-family: Arial, Helvetica, sans-serif;
     }
/* 
     .container {
        width: 650px;
        margin: 0 auto;
     } */

     
    :global(.container) {
        width: 650px;
        margin: 0 auto;
    }
</style>

<div class="container">
    <h1>momo</h1>
    <NavBar/>
</div>
