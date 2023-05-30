<script lang="ts">
    import NavButton from "../components/buttons/nav-button.svelte";
    import trees_pixel_art from "$lib/assets/personal-work/pixel-art/tree.png";


</script>


<section class="things-i-do">
    <section class="nav">
        <h2>Things I Do</h2>
        <div class="buttons">
            <NavButton href="/pixel-art">Pixel Art</NavButton>
            <NavButton href="/minecraft-art">Minecraft Art</NavButton>
            <NavButton href="/game-development">Game Development</NavButton>
        </div>
    </section>
    <div class="image-wrapper">
        <img src={trees_pixel_art} alt="trees">
    </div>
</section>



<style>
    .things-i-do {
        width: 100%;
        background-color: var(--neutral-color-1);
        border-radius: 1rem;

        display: grid;
        grid-auto-flow: column;
        grid-template-columns: 1fr 0.6fr;
        
        justify-content: space-between;

    }

    .nav {
        width: 100%;
        transform: translate(0.5rem, -0.5rem);
    }

    .nav > h2 {
        font-size: x-large;
        margin: 0 0 1rem 0;
        background-color: var(--primary-color-1);
        border-radius: 0 0 4rem 0;

        padding: 0.5rem 2rem 0.5rem 2rem;

        width: 50%;
    }

    .buttons {
        display: flex;
        flex-direction: column;
        gap: 0.2rem;
        width: 70%;
    }

    .image-wrapper {
        background-color: var(--secondary-color-1);
        border-radius: 1rem;
        width: 100%;
    }

    .image-wrapper > img {
        transform: translate(0.5rem, -0.5rem);
        width: 100%;
        border-radius: 1rem;
    }


    @media(max-width: 700px) {
        .nav > h2 {
            font-size: medium;
        }
    }


    @media(max-width: 300px) {
        .image-wrapper {
            height: 10rem;
            width: auto;
        }

        .image-wrapper > img {
            height: 100%;
            width: auto;
        }

        .things-i-do {
            grid-template-columns: 1fr 0.2fr;
        }
    }
</style>