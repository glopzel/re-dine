<script>
    export let name, desc, src;
</script>

<div id='dish' class="flex sm:flex-row flex-col mb-8">
    <div class="img-container">
        <img src={src} alt="">
    </div>
    <div class="sm:pl-10 pl-0">
        <h4 class="heading-m mb-4 text-res sm:mt-0 mt-6">{name}</h4>
        <p class="p-smaller text-res font-thin">{desc}</p>
    </div>
</div>

<style>
    img {
        width: 160px;
        aspect-ratio: 1 / 0.8;
    }
</style>