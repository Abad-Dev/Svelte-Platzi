<script>
    export let img;
</script>

<main>
    <div class="container">
        <div class="row">
            <div class="humanase-bg w-100 justify-content-center d-flex" style="border-radius: 15px;">
                <img src={img} alt="" class="main-img">
            </div>
        </div>
    </div>
</main>

<style>
    .main-img{
        max-width: 70%;
        position: relative;
        top: 15%;
        border: 2px solid #fff;
        padding: 5px;
    }
</style>