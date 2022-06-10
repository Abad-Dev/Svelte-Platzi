<script>
    import { Link } from 'svelte-navigator';
    import logo from './images/logo.jpg';
    import { page } from './store/store';

    let navBar;
    let linksContainer;

    let navOptions = [
        {url: '/', label: 'Home'},
        {url: '/empresa', label: 'La empresa'}, 
        {url: '/servicios', label: 'Servicios'}, 
        {url: '/clientes', label: 'Nuestros Clientes'},
        {url: '/contactenos', label: 'Contáctenos'}
    ]

    const hideNavBar = () => {
        navBar.classList.add('collapsed')
        linksContainer.classList.remove('show')
    }
</script>
  

<main>
    <nav class="navbar navbar-expand-lg navbar-light bg-white" bind:this={navBar}>
        <div class="container">
            <Link to="/" class="navbar-brand d-flex" draggable="false">
                <img src={logo} alt="" draggable="false">
                <div>
                    <h1 class="humanase-text mt-2 mb-0">Humana</h1>
                    <small style="font-size: 13px; float: right;" class="text-muted fw-bold">Socios Estratégicos</small>
                </div>
            </Link>
            <button class="navbar-toggler d-lg-none" type="button" data-bs-toggle="collapse" data-bs-target="#collapsibleNavId" aria-controls="collapsibleNavId" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="collapsibleNavId" bind:this={linksContainer}>
                <ul class="navbar-nav ms-auto mt-2 mt-lg-0">
                    {#each navOptions as route}
                    <li class="nav-item">
                        <Link 
                            to={route.url} 
                            class={`nav-link ${$page === route.url ? 'humanase-active' : ''}`}
                            on:click={() => {hideNavBar(); page.set(route.url)}}
                        >
                            {route.label}
                        </Link>
                    </li>
                    {/each}
                </ul>
            </div>
        </div>
    </nav>
</main>
