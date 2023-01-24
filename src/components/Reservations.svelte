<script>
    import Header from './Header.svelte'

    let count = 1;
    const countPlusOne = () => {
        if (count < 20) {
            count++;
        }
    }

    const countOneLess = () => {
        if (count > 1) {
            count--;
        }
    }
</script>

<main class="">
    <div id='main-container' class="container">
        <Header />
    
        <div id='form-text-container'>
            <section class="text-white">
                <h1 class="heading-l text-res md:heading-xl mb-6 sm:mb4">Reservations</h1>
                <p class="text-center text-res pr-0 sm:pr-6">We can’t wait to host you. If you have any special requirements please feel free to call on the phone number below. We’ll be happy to accommodate you.</p>
            </section>
            
            <section class="">
                <form action="" class="shadow flex flex-col">
                    <label for="name-input"></label>
                    <input type="text" maxlength="22" id='name-input' placeholder='Name' class="mb-8" required/>
                
                    <label for="email-input"></label>
                    <input type="email" name='email-input' id='email-input' placeholder='Email' class="mb-6" required/>
                
                    <div class="inputs-detail">
                        <label for="date">Pick a Date</label>
                        <input class="invalid:border-pink-500 invalid:text-pink-600" min='1' max='12' type="number" name="month" id="month" placeholder='MM' required/>
                        <input class="invalid:border-pink-500 invalid:text-pink-600" type="number" min='1' max='31' name="day" id="day" placeholder='DD' required/>
                        <input class="invalid:border-pink-500 invalid:text-pink-600" type="number" name="year" min='2023' max='2050' id="year" placeholder='YYYY' required/>
                    </div>
                
                    <div class="inputs-detail">
                        <label for="time">Pick a time</label>
                        <input type="number" name="hour" id="hour" placeholder="00" min='1' max='12' required>
                        <input type="number" name="minutes" id="minutes" placeholder="00" min='0' max='59' required>
                        <select name="time-selection" id="time-selection">1
                            <option value="AM">AM</option>
                            <option value="PM">PM</option>
                        </select>
                    </div>
        
                    <div id="count" class="my-6 flex justify-around p-2">
                        <button class="px-2" on:click={countOneLess}>
                            <img src="https://ik.imagekit.io/a8p7pl7hs/dinesite/images/icons/icon-minus_8un3qwSie.svg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487855163" alt="">
                        </button>
                        <span>{`${count} ${count > 1 ? 'people' : 'person'}`}</span> 
                        <button class="px-2" on:click={countPlusOne}>
                            <img src="https://ik.imagekit.io/a8p7pl7hs/dinesite/images/icons/icon-plus_IPRz3fll57.svg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487850784" alt="">
                        </button>   
                    </div>
                
                    <button id="submit-res" class="btn-general dark-btn btn-black">Make Reservation</button>
                </form>
            </section>
        </div>
    </div>
</main>

<style>
    main {
        min-height: 100vh;
        padding-bottom: 2em;
        background-repeat: no-repeat;
        background-size: cover;
        background-position: right;
        display: flex;
    }

    input[type='number'] {
        width: 90%;
        margin-inline: auto;
    }

    h1 {
        margin-top: 1em;
    }

    p {
        margin-bottom: 1em;
    }

    form {
        /* flex flex-col  */
        background: white;
        padding: 1em;
    }

    input, select {
        padding: 0.5em;
        margin: 0.5em;
        border-bottom: 1px solid rgb(92, 103, 121);
        text-align: center;
    }

    #count {
        border-bottom: 1px solid black;
    }

    .inputs-detail {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
    }

    .inputs-detail label {
        text-align: center;
        grid-row: 1/2;
        grid-column: 1/4;
    }

    @media (max-width: 500px) {
        main {
            background-image: url('https://ik.imagekit.io/a8p7pl7hs/dinesite/images/booking/hero-bg-mobile_TWXHhljf5k.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487852815');
            background-size: cover;
        }
    }

    @media (min-width: 500px) and (max-width:  820px) {
        main {
            background-image: url('https://ik.imagekit.io/a8p7pl7hs/dinesite/images/booking/hero-bg-tablet_CjTZ_4m54m.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487851534');
        }
    }

    @media (min-width: 815px) {
        main {
            background-image: url('https://ik.imagekit.io/a8p7pl7hs/dinesite/images/booking/hero-bg-desktop_CKnfGFt3p2.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1674487851231');
        }

        #form-text-container {
            display: flex;
            margin-top: 10vh;
        }

        #form-text-container > * {
            flex: 1;
        }

        h1 {
            margin-top: 0;
        }

        .inputs-detail {
            grid-template-rows: 1fr;
            grid-template-columns: auto repeat(3, 25%);
        }

        .inputs-detail label {
            grid-row: 1/2;
            grid-column: 1/2;
            align-self: center;
        }
    }

    @media (min-width: 1000px) {
        #form-text-container {
            margin-top: 20vh;
        }
    }
</style>