<script lang="ts">
    import "./+page.css"

    import picture_felipe from "$lib/assets/picture-felipe.jpg";
    import trees_pixel_art from "$lib/assets/personal-work/pixel-art/tree.png";

    import xp_logo from "$lib/assets/marketplace-teams/xp-games.jpg";
    import spark_logo from "$lib/assets/marketplace-teams/spark-universe.jpg";
    import tinkrew_logo from "$lib/assets/marketplace-teams/tinkrew.jpg";
    import eternal_logo from "$lib/assets/marketplace-teams/eternal-creations.jpg";

    import cube_icon from "$lib/assets/icons/cube.svg";
    import game_dev_icon from "$lib/assets/icons/game_dev.svg";
    import pixel_art_icon from "$lib/assets/icons/pixel_art.svg";
	import LetsWorkButton from "../components/buttons/lets-work-button.svelte";



    var age = 18;

</script>


<main>
    <header>
        <div class="image-wrapper">
            <img src={picture_felipe} alt="Felipe">
        </div>
        <div class="text">
            <h1>Felipe de Souza, 18</h1>
            <p><i>&gt I'm here to help bring your ideas to life</i></p>
            <LetsWorkButton></LetsWorkButton>
        </div>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" fill="var(--neutral-color-1)"></path></svg>
    </header>

    <section class="what-i-do">
        <section class="nav">
            <h2>What I Do</h2>
            <div class="buttons">
                <a class="button" id="button0" href="/pixel-art">Pixel Art</a>
                <a class="button" id="button1" href="/minecraft-art">Minecraft Art</a>
                <a class="button" id="button2" href="/game-dev">Game Development</a>
            </div>
        </section>
        <div class="image-wrapper">
            <img src={trees_pixel_art} alt="trees">
        </div>
    </section>
    
</main>


<style>
    main {
        display: flex;
        flex-direction: column;

        place-items: center;
        justify-content: center;
        height: 100%;
        gap: 3rem;

        margin: 0 8rem 0 8rem;
    }

    header {
        display: grid;
        grid-auto-flow: column;
        place-items: center;
        justify-content: left;

        position: relative;

        width: 100%;

        grid-template-rows: 20rem;
    }

    header > svg {
        z-index: -1;
        position: absolute;
        scale: 50%;
    }

    .image-wrapper {
        background-color: var(--secondary-color-1);
        border-radius: 1rem;
        height: 100%;
    }

    .image-wrapper > img {
        transform: translate(0.5rem, -0.5rem);
        height: 100%;
        border-radius: 1rem;
    }

    .text {
        margin-top: 2rem;
        display: grid;
        grid-template-rows: auto;
        grid-template-columns: 100%;
    }

    .text > h1, p {
        margin: 0 0 0 0;
        padding-left: 1rem;
    }

    .text > h1 {
        background-color: var(--primary-color-1);
        margin-bottom: 0.5rem;
        padding: 0.5rem 2rem 0.5rem 2rem;
    }


    .what-i-do {
        width: 100%;
        height: 15rem;

        display: grid;
        grid-auto-flow: column;
        grid-template-columns: 20rem 15rem;
        grid-template-rows: 15rem;

        justify-content: space-between;
    }

    .nav {
        width: 100%;
        font-size: x-large;
    }

    .nav > h2 {
        margin: 1rem 0 1rem 0;
        background-color: var(--primary-color-1);
        padding: 0.5rem 2rem 0.5rem 2rem;
    }

    .buttons {
        display: flex;
        flex-direction: column;
    }

    .button {
        all: unset;
        padding: 0.5rem 0 0.5rem 1rem;
        text-align: left;
        border-radius: 1rem;
        transition: 200ms ease-in;
    }

    .button:hover {
        background-color: var(--neutral-color-1);
        padding-left: 1.5rem;
    }

    .buttons > #button0 {

    }

    @media(max-width: 1100px) {
        main {
            margin: 1rem;
        }
    }

    @media(max-width: 800px) {
        main {
            gap: 5rem;
        }
        
        header {
            grid-auto-flow: column;
            grid-template-rows: 15rem;
            grid-template-columns: 15rem auto;
        }

        .text {
            width: 100%;
        }

        .text > h1 {
            padding: 0.5rem;
            padding-left: 1.5rem;
        }

        .text > p {
            font-size: x-large;
        }

        .what-i-do {
            gap: 1rem;
        }

        .nav > h2 {
            margin: 0;
        }
    }

</style>