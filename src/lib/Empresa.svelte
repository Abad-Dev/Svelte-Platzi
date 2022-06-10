<script>
    import Main from './Main.svelte';
    import empresaImg from './images/main2.jpg';
    import equipo from './images/equipo.png';
</script>

<main>
    <Main img={empresaImg}/>
    
    <div class="container my-5 pt-0 pt-lg-4 text-secondary text-center text-lg-start">
        <div class="row">
            <div class="col-12 my-4">
                <h5>• Visión</h5>
                <p>Ser reconocida por nuestros clientes, socios y empresas, como la mejor<br>
                    consultora en el desarrollo del talento.</p>
            </div>
            <div class="col-12 ">
                <h5>• Misión</h5>
                <p>Contribuir con soluciones especialmente desarrolladas para cada necesidad de nuestros clientes. Brindando un servicio diferenciado, de alta<br>
                    calidad y excelencia, que nos convierta en socios estratégicos en el logro de sus objetivos.</p>
            </div>
        </div>
        <hr>
        <div class="row align-items-center">
            <div class="col-12 col-lg-6">
                <h5>Nuestra Diferencia</h5>
                <p>Desarrollamos planes de mejora de acuerdo a los requerimientos y necesidades que desea cubrir cada uno de nuestros clientes y socios. Contamos con profesionales especializados en las principales áreas empresariales para así obtener una eficiente solución para cada necesidad.</p>
            </div>
            <div class="col-12 col-lg-6 text-center">
                <img src={equipo} alt="" class="mt-2">
            </div>
        </div>            
    </div>
</main>