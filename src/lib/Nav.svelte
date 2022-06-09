<script>
    import { Link } from 'svelte-navigator';
    import logo from './images/logo.jpg';

    let navBar;
    let linksContainer;

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
                    <li class="nav-item">
                        <Link to="/" class="nav-link humanase-hover" on:click={hideNavBar}>Home</Link>
                    </li>
                    <li class="nav-item">
                        <Link to="/empresa" class="nav-link humanase-hover" on:click={hideNavBar}>La empresa</Link>
                    </li>
                    <li class="nav-item">
                        <Link to="/servicios" class="nav-link humanase-hover" on:click={hideNavBar}>Servicios</Link>
                    </li>
                    <li class="nav-item">
                        <Link to="/clientes" class="nav-link humanase-hover" on:click={hideNavBar}>Clientes </Link>
                    </li>
                    <li class="nav-item">
                        <Link to="/contactenos" class="nav-link humanase-hover" on:click={hideNavBar}>Contáctenos</Link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</main>
