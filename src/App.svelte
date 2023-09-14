<script>
  import { Router, Link, Route } from "svelte-routing";


  export let basepath = "/prode-svelte";

</script>

<main>
<Router {basepath}>
  <nav>
    <Link to="/">Home</Link>
    <Link to="/about">About</Link>
    <Link to="/blog">Blog</Link>
  </nav>
  <div>
    <Route path="/blog/:id" component={BlogPost} />
    <Route path="/blog" component={Blog} />
    <Route path="/about" component={About} />
    <Route path="/"><Home /></Route>
  </div>
</Router>
</main>

<style>
 
</style>
