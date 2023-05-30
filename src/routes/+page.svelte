<script lang="ts">
    import "./header.css"
    import "./things-i-do.css"

    import picture_felipe from "$lib/assets/picture-felipe.jpg";
    import trees_pixel_art from "$lib/assets/personal-work/pixel-art/tree.png";
	import LetsWorkButton from "../components/buttons/lets-work-button.svelte";
	import NavButton from "../components/buttons/nav-button.svelte";



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



    @media(max-width: 1100px) {
        main {
            margin: 1rem;
        }
    }

    @media(max-width: 700px) {
        .text > h1 {
            font-size: large;
            padding: 0.5rem 0 0.5rem 1rem;
        }

        .text > p {
            font-size: small;
        }

        .nav > h2 {
            font-size: medium;
        }
    }

    @media(max-width: 300px) {
        main {
            margin: 0;
        }

        header {
            grid-auto-flow: row;
            grid-template-rows: 1fr auto;
            grid-template-columns: 100%;
            gap: 1rem;

            justify-items: center;

        }
        
        .text > p {
            padding: 0;
        }

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