<script>
    import { Link } from 'svelte-navigator'
    import Main from './Main.svelte';
    import homeImg from './images/main1.jpg';
    import iniCoach from './images/inicoach.jpg';
    import capacitaciones from './images/capacitaciones.jpg';
    import outplacement from './images/outplacement.jpg';
    import coaching from './images/coaching.jpg';
</script>

<main>
    <Main img={homeImg}/>

    <div class="container  mt-5 pt-0 pt-lg-4 text-secondary">
        <div class="row align-items-center">
            <div class="col-12 col-lg-8 text-center text-lg-start">
                <h4 class="humanase-active">Quienes Somos?</h4>
                <p>Humana Socios Estratégicos es una consultora especializada en la gestión del talento. Somos socios estratégicos de empresas líderes, que buscan lograr que sus organizaciones y colaboradores desarrollen al máximo su potencial y hagan realidad sus objetivos empresariales.</p>
            </div>
            <div class="col-12 col-lg-4  justify-content-center d-flex">
                <img src={iniCoach} alt="">
            </div>
        </div>
        <hr>
        <div class="row text-center text-md-start my-4">
            <div class="col-12 col-md-4">
                <h5 class="humanase-active">Capacitaciones</h5>
                <img src={capacitaciones} class="mx-auto my-2 d-block" alt="">
                <p class="text-lg-start">Escuelas Corporativas, Outdoor, Programas, Talleres, Cursos. Trabajo en equipo, estrategias...</p>
                <div class="text-md-end mt-2 mb-5 pe-md-3 wrapper">
                    <Link to="/servicios/capacitaciones" class="btn humanase-outline-btn">Ver más ➜</Link>
                </div>
            </div>
            <div class="col-12 col-md-4">
                <h5 class="humanase-active">Coaching</h5>
                <img src={coaching} class="mx-auto d-block" alt="">
                <p>Trabajar y mejorar los aspectos destacados por el jefe inmediato patrocinador y coachee...</p>
                <div class="text-md-end mt-2 mb-5 pe-md-3 wrapper">
                    <Link to="/servicios/coaching" class="btn humanase-outline-btn">Ver más ➜</Link>
                </div>
            </div>
            <div class="col-12 col-md-4">
                <h5 class="humanase-active">Outplacement</h5>
                <img src={outplacement} class="mx-auto d-block" alt="">
                <p>Aumente sus probabilidades de reinserción laboral o redireccione su carrera profesional...</p>
                <div class="text-md-end mt-2 mb-5 pe-md-3 wrapper">
                    <Link to="/servicios/outplacement" class="btn humanase-outline-btn">Ver más ➜</Link>
                </div>
            </div>
        </div>
    </div>

</main>


<style>
    .wrapper :global(.humanase-outline-btn) {
        color: var(--humanase-green);
        border-color: var(--humanase-green);
        transition-duration: .2s;
    }

    .wrapper :global(.humanase-outline-btn):hover{
        background-color: var(--humanase-green);
        color: #fff
    }
</style>
