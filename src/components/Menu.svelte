<script>
    import Dish from "./Dish.svelte";
</script>

<div id="menu-section" class="dark-block padding-block-xxl">
    <div class="even-cols container">
        <section class='highlights-text'>
            <h3 class="heading-l text-res mb-4">A few highlights from our menu</h3>
            <p class="p-bigger text-res">We cater for all dietary requirements, but here’s a glimpse at some of our diner’s favourites. Our menu is revamped every season.</p>
        </section>
        
        <div id='dish-container' class="">
            <Dish name='Seared Salmon Fillet' desc='Our locally sourced salmon served with a refreshing buckwheat summer salad.' src='https://ik.imagekit.io/a8p7pl7hs/dinesite/images/homepage/salmon-mobile_2x_IQwlz7OsX.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1674497522161'/>
            <Dish name='Rosemary Filet Mignon' desc='Our prime beef served to your taste with a delicious choice of seasonal sides.' src='https://ik.imagekit.io/a8p7pl7hs/dinesite/images/homepage/beef-desktop-tablet_7NqX4gM4u6.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487881835'/>
            <Dish name='Summer Fruit Chocolate Mousse' desc='Creamy mousse combined with summer fruits and dark chocolate shavings.' src='https://ik.imagekit.io/a8p7pl7hs/dinesite/images/homepage/chocolate-desktop-tablet_mKu5zncYUr.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487857766'/>
        </div>
    </div>
</div>

<style>
    #dish-container {
        display: grid;
    }
    @media (min-width: 50em) {
        .highlights-text {
            padding-right: 2em;
        }
    }
    /* .menu-section? */
</style>