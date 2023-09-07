<script lang="ts">
	import Header from "./header.svelte";


    import dragon_pixelart from "$lib/assets/personal-work/pixel-art/dragon.png";
    import shark_pixelart from "$lib/assets/personal-work/pixel-art/shark.png";
    import moth_pixelart from "$lib/assets/personal-work/pixel-art/moth.png";
    import jurassic_park from "$lib/assets/personal-work/pixel-art/jurassic-park.png";
    import kelp_forest from "$lib/assets/personal-work/pixel-art/kelp-forest.png";
    import morning_mountains from "$lib/assets/personal-work/pixel-art/morning-mountains.png";
    import war_landscape from "$lib/assets/personal-work/pixel-art/war-landscape.png";
    import frajola from "$lib/assets/personal-work/pixel-art/frajola.png";
    import pop from "$lib/assets/commissioned-work/popvtuber/loading_screen.gif";
    
 
	import LinkButton from "../components/buttons/link_button.svelte";

</script>


<Header></Header>



<section class="showcase">
    <div class="nav-wrapper">
        <nav>
            <button class="medium-text">Pixel Art</button>
            <button class="medium-text">Minecraft</button>
            <button class="medium-text">Game Dev</button>
        </nav>
    </div>
    <div class="art-pieces">
        <img class="long-image left" src={kelp_forest} alt="">
        <img class="long-image" src={pop} alt="">
        <img src={shark_pixelart} alt="">
        <img src={dragon_pixelart} alt="">
        <img src={morning_mountains} alt="">
        <img src={frajola} alt="">
    </div>
</section>





<style>
    .showcase {
        margin-bottom: 2rem;
        margin-top: 2rem;
    }

    .showcase > .nav-wrapper {
        display: flex;
        place-content: center;
    }

    .nav-wrapper > nav {
        display: flex;
        gap: min(5vw, 5ch);

        margin-top: 0;
        margin-bottom: 2rem;
    }

    .nav-wrapper > nav > button {
        background-color: transparent;
        border: none;
        border-bottom: 0.2ch solid var(--neutral-color-0);
        color: white;
        place-self: center;
        text-align: center;
        transition: 400ms ease-out;
    }

    .nav-wrapper > nav > button:hover {
        border-bottom: 0.2ch solid white;
        transition: 200ms;
    }
    
    .art-pieces {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 1rem;
    }

    .art-pieces > img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border: 0.2ch solid var(--neutral-color-1);
        grid-column: span 2;
    }

    .art-pieces > .long-image {
        grid-column: span 4;
    }

    .left {
        object-position: left;
    }
</style>