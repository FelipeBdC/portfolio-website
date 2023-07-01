<script lang="ts">
	import Header from "./header.svelte";


    import dragon_pixelart from "$lib/assets/personal-work/pixel-art/dragon.png";
    import shark_pixelart from "$lib/assets/personal-work/pixel-art/shark.png";
    import moth_pixelart from "$lib/assets/personal-work/pixel-art/moth.png";
    import jurassic_park from "$lib/assets/personal-work/pixel-art/jurassic-park.png";
 
	import LinkButton from "../components/buttons/link_button.svelte";

</script>


<Header></Header>



<section class="showcase">
    <section class="top-bar">
        <!-- <nav>
            <button>Pixel Art</button>
            <button>Minecraft</button>
            <button>Game Dev</button>
        </nav> -->
        <LinkButton text="See More" url="/gallery"></LinkButton>
    </section>
    <div class="art-pieces">
        <img class="long-image left" src={jurassic_park} alt="">
        <img src={shark_pixelart} alt="">
        <img src={dragon_pixelart} alt="">
        <img class="long-image" src={moth_pixelart} alt="">
    </div>
</section>





<style>
    h1 {
        margin: 0;
    }



    .showcase {
        margin-bottom: 2rem;
        border: 2px solid var(--neutral-color-1);
        padding: min(2vh, 2rem);
    }


    .top-bar {
        display: flex;
        justify-content: space-between;
        margin-bottom: min(2vh, 2rem);
    }
    h1 {
        font-size: min(6vw, 2rem);
        place-self: center;
    }
    .top-bar > nav {
        display: grid;
        grid-auto-flow: column;
        place-items: center;
        gap: 1rem;
    }
    .top-bar > nav > button {
        all: unset;
        padding: min(5vw, 0.5rem) min(8vw, 2rem) min(5vw, 0.5rem) min(8vw, 2rem);
        border: 2px solid var(--neutral-color-2);
        color: white;
        border-radius: 0.5rem;

        cursor: pointer;

        place-self: center;
        transition: 200ms ease-in;
    }
    .top-bar > nav > button:hover {
        background-color: var(--neutral-color-2);
        border-color: var(--neutral-color-2);
        color: white;
        transition: 200ms ease-out;
    }

    .top-bar > nav > button:focus {
        background-color: white;
        border-color: white;
        color: black;
        transition: 200ms ease-out;
    }
    
    .art-pieces {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 1rem;
    }

    .art-pieces > img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border: 2px solid var(--neutral-color-1);
    }

    .art-pieces > .long-image {
        grid-column: span 2;
    }

    .left {
        object-position: left;
    }
</style>