<script>
  import { Route, Router } from 'svelte-navigator';
  import Nav from './lib/Nav.svelte'
</script>

<main>
  <Router>

    <Nav />

    <Route path="/">
      <h1>Hola mundo</h1>
    </Route>

    <Route path="/empresa">
      <h2>Esta es la empresa</h2>
    </Route>

  </Router>
</main>

<style>
  :global(html){
    border-top: 10px solid rgb(111, 184, 61);
    min-height: 100%;
  }
  :global(.humanase-text){
    color: rgb(111, 184, 61);
  }
  :global(.humanase-hover:hover){
    color: rgb(111, 184, 61);
  }
</style>
