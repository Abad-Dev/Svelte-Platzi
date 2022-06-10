<script>
  // @ts-ignore
  import { Route, Router } from 'svelte-navigator';
  import Nav from './lib/Nav.svelte';
  import Home from './lib/Home.svelte';
  import Empresa from './lib/Empresa.svelte';
</script>

<main>
  <Router>

    <Nav />

    <Route path="/" primary={false}>
      <Home />
    </Route>

    <Route path="/empresa" primary={false}>
      <Empresa />
    </Route>

  </Router>
</main>

<style>
  :global(:root){
    --humanase-green: rgb(111, 184, 61);
  }
  :global(html){
    border-top: 11px solid var(--humanase-green);
    min-height: 100%;
  }
  :global(.humanase-text){
    color: var(--humanase-green);
  }
  :global(.humanase-hover:hover){
    color: var(--humanase-green);
  }
  :global(.humanase-bg){
    background-color: var(--humanase-green);
  }
  :global(.humanase-active){
    color: var(--humanase-green);
    text-decoration: 2px underline var(--humanase-green);
  }
  :global(img){
    max-width: 65%;
    height: auto;
  }
</style>
