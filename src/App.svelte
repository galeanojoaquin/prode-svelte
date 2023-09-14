<script>
  import { Router, Link, Route } from "svelte-routing";
  import NotFound from "./components/Layout/NotFound.svelte";
  import Index from "./components/Index/Index.svelte";

  export let basepath = "/prode-svelte";
</script>

<main>
  <Router {basepath}>
    <nav>
      <Link to="/about">About</Link>
      <Link to="/blog">Blog</Link>
    </nav>
    <div class="container">
      <div class="container pb-5 mb-5">
        <div>
          <Route path="/" component={Index}/>
          <Route path="/*" component={NotFound} />
        </div>
      </div>
    </div>
  </Router>
</main>

<style>
</style>
