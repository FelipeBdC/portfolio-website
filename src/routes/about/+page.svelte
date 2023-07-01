<script lang="ts">
    import picture_felipe from "$lib/assets/picture-felipe.jpg";
    import aseprite_icon from "$lib/assets/icons/aseprite-svgrepo-com.svg";
    import blockbench_icon from "$lib/assets/icons/blockbench_logo_white.svg";

    import kubo_studios_logo from "$lib/assets/marketplace-teams/kubo-studios.jpg";
    import eternal_creations_logo from "$lib/assets/marketplace-teams/eternal-creations.jpg";
    import spark_universe_logo from "$lib/assets/marketplace-teams/spark-universe.jpg";
    import xp_games_logo from "$lib/assets/marketplace-teams/xp-games.jpg";

    let marketplace_starting_year: number = 2020;
    let gamedev_starting_year: number = 2019;

    let current_date: Date = new Date();
    let current_year: number = current_date.getFullYear();
    let time_in_marketplate: number = current_year - marketplace_starting_year;
    let time_in_gamedev: number = current_year - gamedev_starting_year;
</script>


<header>
    <img src={picture_felipe} alt="Felipe">
    <section>
        <div class="big-text text-centered">Hello!</div>
        <p class="small-text text-justify">
            My name is Felipe de Souza, i'm a young and passionate
            pixel artist! I have worked for {time_in_marketplate} years on the Minecraft
            Marketplace, helping various teams bring life to their worlds
        </p>
        <p class="small-text text-justify">
            I also have {time_in_gamedev} years of experience doing Video Game Art, but
            I've never had a chance to do it professionally.
        </p>
    </section>
</header>

<main>
    <section>
        <div class="medium-text text-centered">Software I use</div>
        <div class="icons">
            <img id="aseprite-icon" class="program-icon" src={aseprite_icon} alt="Aseprite">
            <img class="program-icon" src={blockbench_icon} alt="Blockbench">
        </div>
    </section>
    
    <section>
        <div class="medium-text text-centered">
            Teams I've collaborated with
        </div>
        <div class="icons">
            <img class="program-icon icon-border" src={xp_games_logo} alt="">
            <img class="program-icon icon-border" src={spark_universe_logo} alt="">
            <img class="program-icon icon-border" src={eternal_creations_logo} alt="">
            <img class="program-icon icon-border" src={kubo_studios_logo} alt="">
        </div>
    </section>
</main>



<style>

    header {
        display: grid;
        grid-auto-flow: column;
        grid-auto-columns: 1fr;
        gap: 1rem;

        margin-top: 2rem;
        margin-bottom: 4rem;
    }

    header > img {
        min-height: 50dvh;
        height: 40dvh;
        width: 100%;
        object-fit: cover;
        object-position: 50% 80%;
        padding: 0.4rem;
        border: 2px solid var(--neutral-color-1);
        box-sizing: border-box;
    }


    main {
        display: grid;
        grid-auto-flow: column;
        grid-auto-columns: 1fr;
        gap: min(3vh, 1rem);
    }

    main > section {
        padding: 1rem;
        border: 2px solid var(--neutral-color-1);
    }

    .icons {
        margin-top: 1rem;
        display: flex;
        place-content: space-evenly;
    }

    .program-icon {
        width: min(8ch, 10vw);
    }
    #aseprite-icon {
        width: min(6ch, 8vw);
    }

    .icon-border {
        border: 2px solid var(--neutral-color-1);
        border-radius: 1rem;
        padding: 2px;
    }


    @media(max-width: 700px) {
        header {
            grid-auto-flow: row;
        }

        main {
            display: flex;
            flex-direction: column;
        }
    }
</style>