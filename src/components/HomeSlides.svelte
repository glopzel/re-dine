<script>
    let src, title, content;
    src = 'https://ik.imagekit.io/a8p7pl7hs/dinesite/images/homepage/family-gathering-desktop_341paFVSBs.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487859335'
    title='Family Gathering'
    content="We love catering for entire families. So please bring everyone along for a special meal with your loved ones. We’ll provide a memorable experience for all.";
    let current = 'family';

    const familyClick = () => {
        src = 'https://ik.imagekit.io/a8p7pl7hs/dinesite/images/homepage/family-gathering-desktop_341paFVSBs.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487859335'
        title='Family Gathering'
        content="We love catering for entire families. So please bring everyone along for a special meal with your loved ones. We’ll provide a memorable experience for all."
    }

    const specialEventsClick = () => {
        src='https://ik.imagekit.io/a8p7pl7hs/dinesite/images/homepage/special-events-mobile_2x_dVcZBqaOG.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487858456'
        title='Special Events'
        content="Whether it’s a romantic dinner or special date you’re celebrating with others we’ll look after you. We’ll be sure to mark your special date with an unforgettable meal."
    }

    const socialEventsClick = () => {
        src='https://ik.imagekit.io/a8p7pl7hs/dinesite/images/homepage/social-events-desktop_2x_rejlSDm3Eh.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487859288'
        title='Social Events'
        content="Are you looking to have a larger social event? No problem! We’re more than happy to cater for big parties. We’ll work with you to make your event a hit with everyone."
    }
</script>

<div class="padding-block-xl">
    <section class="container even-cols items-between">
        <div>
            <img src={src} alt="" class="shadow" id="img-toggled"/>
        </div>

        <div id="content-toggled" class="">
            <div id="descriptions-toggled" class="padding-section">
                <h4 class="heading-l text-res">{title}</h4>
                <p class="p-bigger text-res">{content}</p>
                <div class="book-btn-container">
                    <button class="">
                        <a href="/reservations" class="btn-general btn-black">Book a table</a>
                    </button>
                </div>
            </div>
            <div id="toggle-btn-container" class="">
                <ul id='toggle-btns' class="padding-section">
                    <li class="py-2">
                        <button class={current === 'family' ? 'selected border-selected': 'not-selected'} on:click={() => {
                            familyClick();
                            current = 'family';
                        }}>Family Gathering</button>
                    </li>
    
                    <li class="py-2">
                        <button class={current === 'special' ? 'selected border-selected': 'not-selected'} on:click={() => {
                            specialEventsClick()
                            current = 'special'
                        }}>Special Events</button>
                    </li>
                    <li class="py-2">
                        <button class={current === 'social' ? 'selected border-selected': 'not-selected'} on:click={() => {
                            socialEventsClick();
                            current = 'social';
                        }}>Social Events</button>
                    </li>
                </ul>
            </div>
        </div>
    </section>    
</div>

<style>
    p {
        color: #242B37;
    }

    .not-selected {
        opacity: 0.5;
    }

    .book-btn-container {
        margin-inline: auto;
    }

    .border-selected {
        border-bottom: 1px solid rgb(158, 127, 102);
    }

    #descriptions-toggled {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
    }

    #content-toggled {
        display: grid;
        grid-template-rows: repeat(2, auto);
    }

    #toggle-btn-container {
        grid-row: 1/2;
        display: flex;
        align-items: flex-start;
        margin-top: 2em;
    }

    #toggle-btns {
        display: flex;
        justify-content: space-between;
        margin-top: 4px;
        width: 100%;
    }

    #toggle-btns li {
        display: flex;
        align-items: center;
    }

    @media (max-width: 500px) {
        #toggle-btns {
            flex-direction: column;
            align-items: center;
        }
    }

    @media (min-width: 50em) {
        .book-btn-container {
            margin-inline: 0;
        }

        .padding-section {
            padding-left: 2em;
        }

        #toggle-btn-container {
            align-items: flex-end;
            grid-row: 2/3;
        }

        #toggle-btns {
            flex-direction: column;
            justify-content: center;
            margin-top: 4px;
            widows: 100%;
        }

    }
</style>