<script>
  // @ts-ignore
  import { Route, Router } from 'svelte-navigator';
  import Nav from './lib/Nav.svelte';
  import Footer from './lib/Footer.svelte';
  import Home from './lib/Home.svelte';
  import Empresa from './lib/Empresa.svelte';
  import Servicios from './lib/Servicios.svelte';
</script>

<main class="appContainer">
  <Router>

    <Nav />

    <Route path="/" primary={false}>
      <Home />
    </Route>

    <Route path="/empresa" primary={false}>
      <Empresa />
    </Route>

    <Route path='/servicios' primary={false}>
      <Servicios />
    </Route>

    <Footer />
  </Router>
</main>

<style>
  :global(:root){
    --humanase-green: rgb(111, 184, 61);
  }
  :global(html){
    box-shadow: 0px 11px 0px 0px var(--humanase-green) inset;
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

  :global(#app){
    min-height: 100vh;
  }
  :global(body){
    min-height: 100vh;
  }
  .appContainer{
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
</style>
