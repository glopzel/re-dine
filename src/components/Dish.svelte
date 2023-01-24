<script>
    export let name, desc, src;
</script>

<!-- flex sm:flex-row flex-col mb-8 -->
<div id='dish' class="">
    <div class="img-container">
        <img src={src} alt="">
    </div>
    <div class="">
        <h4 class="heading-m text-res">{name}</h4>
        <p class="p-smaller text-res">{desc}</p>
    </div>
</div>

<style>
    img {
        width: 160px;
        aspect-ratio: 1 / 0.8;
    }

    /* @media (min-width: 50em){

    } */
</style>