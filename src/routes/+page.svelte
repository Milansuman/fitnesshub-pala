<script lang="ts">
    import MobileNav from "$lib/components/mobile-nav.svelte";
    import Button from "$lib/components/ui/button/button.svelte";
    import Carousel from "$lib/Carousel.svelte";

    let open = false;

    const images = [
        "/gym-1.webp",
        "/gym-2.webp",
        "/gym-3.webp",
        "/gym-4.webp",
        "/gym-5.webp",
        "/gym-6.webp",
        "/gym-7.webp",
        "/gym-8.webp",
        "/gym-9.webp",
        "/gym-10.webp",
        "/gym-11.webp",
        "/gym-12.webp",
        "/gym-13.webp",
        "/gym-14.webp",
        "/gym-15.webp",
        // "/gym-16.webp",
        "/gym-17.webp",
        "/gym-18.webp",
        "/gym-19.webp",
        "/gym-20.webp"
    ];
</script>

<main class="bg-black text-neutral-100 w-full h-full overflow-auto">
    <MobileNav open={open} on:closed={() => {open = false}}/>
    <nav class="p-5 flex flex-row justify-between items-center absolute w-full z-10 ">
        <img src="/logo-green.webp" alt="fitness hub logo" class="w-16"/>
        <Button class="rounded-full bg-[#84DF63] text-black font-[400] px-5 hover:bg-[#6cb153] lg:hidden" on:click={() => {open = true}}>Menu</Button>
        <div class="flex-row ml-auto hidden lg:flex gap-3 text-[#84DF63]">
            <a href="#hero" class="hover:underline">Home</a>
            <a href="#about" class="hover:underline">About Us</a>
            <a href="#services" class="hover:underline">Our Services</a>
            <a href="#visit" class="hover:underline">Visit Us</a>
        </div>
    </nav>
    <section id="hero" class=" w-full min-h-screen p-5 flex flex-col gap-3 justify-center items-center">
        <h1 class="font-[900] text-5xl text-center text-[#84DF63] xl:w-96"><i>UNLEASH YOUR POTENTIAL</i></h1>
        <p class="text-neutral-400 text-center text-sm">Start your journey to becoming the best version of yourself.</p>
        <a href="https://wa.me/919846859731?text=Hello!%20I%20would%20like%20to%20start%20a%20membership%20at%20fitness%20hub.">
            <Button class="bg-[#84DF63] text-black font-[600] focus:bg-[#84DF63] hover:bg-[#6cb153]">Get Started</Button>
        </a>
    </section>
    <section id="about" class="mt-6 w-full min-h-screen p-5 flex flex-col gap-3 items-center justify-center">
        <div class="flex flex-col gap-3 md:flex-row md:p-8 justify-center items-center md:items-start">
            <div class="flex flex-col md:w-1/2 gap-3">
                <h1 class="font-[900] text-5xl text-center md:text-left text-[#84DF63]"><i>KNOW YOUR GYM</i></h1>
                <p class="text-neutral-400 text-justify text-sm">
                    Vishnu Vincent, a certified personal trainer with a BSc in Zoology from the Kerala State Body Building Association, offers a range of fitness services including weight gain, weight loss, body shaping, and general fitness. The gym is fully equipped with modern machinery such as treadmills, cycling stations, elliptical machines, rowing machines, and kickboxing gear. As part of the package, clients can enjoy a free diet plan, general training, and a personalized workout plan, with specialized programs designed for diabetic and sugar patients.<br/><br/> In addition to the fitness services, the gym provides excellent amenities for a comfortable experience. These include washrooms, dressing rooms, and resting areas. There are also options to watch movies and sports while working out. For added security, surveillance cameras are installed for women's safety.
                </p>
                <div class="h-full w-full border-l border-[#84DF63] text-[#84DF63] p-3">
                    Open Monday to Saturday, 5 am to 10 pm. (Trainer available from 4 pm to 10 pm)<br/>
                    Whatsapp: <a href="https://wa.me/919846859731?text=Hello!%20I%20would%20like%20to%20start%20a%20membership%20at%20fitness%20hub." class="underline">9846859731</a><br/>
                    Phone: <a href="tel:+918075470633" class="underline">8075470633</a><br/>
                    Instagram: <a href="https://www.instagram.com/fitness_h_u_b_pala/" class="underline">@fitness_h_u_b_pala</a>
                </div>
            </div>
            <Carousel images={images} className="md:w-1/2 max-w-96"/>
        </div>
    </section>
    <section id="services" class=" w-full min-h-screen p-5 flex flex-col gap-3 justify-center items-center">
        <h1 class="font-[900] text-5xl text-center md:text-left text-[#84DF63]"><i>SERVICES WE PROVIDE</i></h1>
        <div class="flex flex-row flex-wrap gap-2 w-full justify-center">
            <div id="weight" class="rounded-md w-full aspect-square flex flex-col p-3 grayscale hover:grayscale-0 max-w-96">
                <p class="mt-auto font-bold text-lg">Weight gain/Weight loss</p>
            </div>
            <div id="body" class="rounded-md w-full aspect-square flex flex-col p-3 grayscale hover:grayscale-0 max-w-96">
                <p class="mt-auto font-bold text-lg">Body Building</p>
            </div>
            <div id="cardio" class="rounded-md w-full aspect-square flex flex-col p-3 grayscale hover:grayscale-0 max-w-96">
                <p class="mt-auto font-bold text-lg">Cardio</p>
            </div>
            <div id="kick" class="rounded-md w-full aspect-square flex flex-col p-3 grayscale hover:grayscale-0 max-w-96">
                <p class="mt-auto font-bold text-lg">Kickboxing</p>
            </div>
            <div id="custom" class="rounded-md w-full aspect-square flex flex-col p-3 grayscale hover:grayscale-0 max-w-96">
                <p class="mt-auto font-bold text-lg">Custom Workout Plans</p>
            </div>
        </div>
    </section>
    <section id="visit" class="w-full p-5 flex flex-col gap-3 justify-center items-center">
        <h1 class="font-[900] text-5xl text-center md:text-left text-[#84DF63]"><i>VISIT US</i></h1>
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d31460.469182738812!2d76.6359449145214!3d9.718657299999995!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3b07cd9d0d93662f%3A0x12f94c0b6e47bcbc!2sFitness%20Hub%20Gymnasium!5e0!3m2!1sen!2sin!4v1727615411079!5m2!1sen!2sin" width="600" height="450" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade" class="w-full rounded-md" title="map"></iframe>
    </section>
    <footer class="p-5 border-t border-[#84DF63] text-[#84df63b3] w-full flex flex-col gap-3">
        <img src="/logo-green.webp" alt="fitness hub logo" class="w-16"/>
        <div class="flex flex-col gap-3 md:flex-row justify-between w-full">
            <div class="md:w-1/2">
                <address>
                    2nd Floor, Perunnolil Building, Carmel Hospital Junction, SH 8, Pala-Thodupuzha Rd, Pala, Kerala 686574
                </address>
            </div>
            <div class="md:w-1/2 md:text-right">
                Whatsapp: <a href="https://wa.me/919846859731?text=Hello!%20I%20would%20like%20to%20start%20a%20membership%20at%20fitness%20hub." class="underline">9846859731</a><br/>
                Phone: <a href="tel:+918075470633" class="underline">8075470633</a><br/>
                Instagram: <a href="https://www.instagram.com/fitness_h_u_b_pala/" class="underline">@fitness_h_u_b_pala</a>
            </div>
        </div>
    </footer>
</main>

<style>
    main{
        font-family: "Poppins", Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
        scroll-behavior: smooth;
    }

    #weight{
        background: url("/burrito.webp") no-repeat center / cover;
    }

    #body{
        background: url("/body.webp") no-repeat center / cover;
    }

    #cardio{
        background: url("/cardio.webp") no-repeat center / cover;
    }

    #kick{
        background: url("/kick.webp") no-repeat center / cover;
    }

    #custom{
        color: #000000;
        background: url("/custom.webp") no-repeat center / cover;
    }

    #hero{
        background: linear-gradient(to bottom, #00000049, #000000), url("/hero.webp") no-repeat 45% 50% / 800px;
    }

    @media screen and (min-width: 780px){
        #hero{
            background: linear-gradient(to bottom, #00000049, #000000), url("/hero.webp") no-repeat 70% 10% / 1000px;
        }
    }

    @media screen and (min-width: 1336px){
        #hero{
            background: linear-gradient(to bottom, #00000049, #000000), url("/hero.webp") no-repeat 60% 40% / 1200px;
        }
    }
</style>
