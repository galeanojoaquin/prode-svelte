<script>
  import { Router, Route } from "svelte-routing";
  import NotFound from "./components/Layout/NotFound.svelte";
  import Index from "./components/Index/Index.svelte";
  import Navbar from "./components/Layout/Navbar.svelte";
  import Teams from "./components/Teams/Teams.svelte";
  export let basepath = "/prode-svelte";
</script>

<Router {basepath}>
  <Navbar />
  <main>
    <!-- <nav>
      <Link to="/about">About</Link>
      <Link to="/blog">Blog</Link>
    </nav> -->
    <div class="container">
      <div class="container pb-5 mb-5">
        <div>
          <Route path="/" component={Index} />
          <Route path="/*" component={NotFound} />
          <Route path="/teams" component={Teams} />
        </div>
      </div>
    </div>
  </main>
</Router>

<style>
  :global(*) {
    box-sizing: border-box;
  }
</style>
