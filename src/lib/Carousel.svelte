<script lang="ts">
    import {gsap} from "gsap";
    import {onMount} from "svelte";
    import { cn } from "./utils";
    export let images: string[];
    export let className: string | undefined = undefined;

    let current = 0;
    let imageElem: HTMLImageElement;
    let fadeInOut: gsap.core.Timeline;

    onMount(() => {
        fadeInOut = gsap.timeline({
            onRepeat: () => {
                current = (current+1) % images.length;
            },
            repeat: -1,
            repeatDelay: 2
        });
        fadeInOut.to(".carousel", {
            opacity: 0,
            duration: 0.5
        })
        fadeInOut.to(".carousel", {
            opacity: 1,
            duration: 0.5,
        })

        return () => fadeInOut.pause();
    })
</script>

<div class={cn("flex flex-col gap-3 z-0", className)}>
    <img src={images[current]} alt="gym equipment" class="carousel rounded-md" bind:this={imageElem}/>
    <div class="flex flex-row gap-2 items-center justify-center">
        {#each images as image}
            {#if image == images[current]}
                <div class="rounded-full w-[8px] h-[8px] bg-[#84DF63] opacity-40"></div>
            {:else}
                <div class="rounded-full w-[6px] h-[6px] bg-[#84DF63] opacity-40"></div>
            {/if}
        {/each}
    </div>
</div>