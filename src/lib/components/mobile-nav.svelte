<script lang="ts">
    import {createEventDispatcher} from "svelte";
    import {gsap} from "gsap";
    import {Button} from "$lib/components/ui/button";

    export let open = false;

    const dispatch = createEventDispatcher();

    let mobileNav: HTMLElement;

    function close(){
        open = false;
        dispatch("closed");
    }

    $: if(mobileNav){
        if(open){
            gsap.to(".mobile-nav", {
                height: "100%"
            });
        }else{
            gsap.to(".mobile-nav", {
                height: "0%"
            });
        }
    }
</script>

<div class="mobile-nav absolute w-full bg-[#84DF63] flex flex-col overflow-hidden h-0 z-20" bind:this={mobileNav}>
    <div class="flex flex-row justify-between p-5 items-center">
        <img src="/logo-black.webp" alt="fitness hub logo" class="w-16"/>
        <Button class="rounded-full px-5" on:click={close}>Close</Button>
    </div>
    <div class="flex flex-col p-5 gap-4 font-bold justify-center text-neutral-900 text-4xl">
        <a href="#hero" on:click={close}>Home</a>
        <a href="#about" on:click={close}>About Us</a>
        <a href="#services" on:click={close}>Our Services</a>
        <a href="#visit" on:click={close}>Visit Us</a>
    </div>
    <div class="mt-auto p-5 flex flex-col">
        <a href="https://wa.me/919846859731?text=Hello!%20I%20would%20like%20to%20start%20a%20membership%20at%20fitness%20hub." class="underline">
            <Button class="rounded-full">Whatsapp</Button>
        </a>
    </div>
</div>