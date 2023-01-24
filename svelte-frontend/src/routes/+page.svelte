<script>
    import { Router, Link, Route } from "svelte-routing";

    export let url = "";
</script>
  
<style>
     .nav-link {
        font-family: Arial, Helvetica, sans-serif;
    }

</style>


  <h1>momo</h1>
  
  
  <Router url="{url}">
    <nav>
      <Link class="nav-link" to="/">Home</Link>
      <Link class="nav-link" to="/artwork">Artwork</Link>
      <Link class="nav-link" to="/shop">Shop</Link>
      <Link class="nav-link" to="/about">About</Link>
    </nav>
    <div>
      <Route path="/"></Route>
    </div>
  </Router>