<script lang="ts">
    import "./+page.css"
    import Header from "./header.svelte";

    import trees_pixel_art from "$lib/assets/personal-work/pixel-art/trees.png";
    import MpTeamCard from "../components/cards/mp-team-card.svelte";
	import NavButton from "../components/buttons/nav-button.svelte";

    import cube_icon from "$lib/assets/icons/cube.svg";
    import game_dev_icon from "$lib/assets/icons/game_dev.svg";
    import pixel_art_icon from "$lib/assets/icons/pixel_art.svg";

</script>


<Header></Header>


<section class="about-me">
    <div class="image-wrapper">
        <img src={trees_pixel_art} alt="Pixel-Art Trees">
    </div>
    <div class="text">
        <h1>About Me</h1>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Omnis voluptate nobis officiis sapiente nisi incidunt cumque maiores fuga quia et qui magni, doloribus repudiandae aperiam, modi esse, voluptatum dolores libero! Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum recusandae nobis natus, odio cumque maxime? Vel optio doloribus ad dicta dignissimos ullam id obcaecati delectus, nesciunt natus odio ex nulla!</p>
    </div>
</section>

<section class="previous-work">
    <h1>Where I Worked</h1>
    <ul class="contractors">
        <MpTeamCard logo="src/lib/assets/marketplace-teams/xp-games.jpg" team_name="XP Games" description="as an Artist"></MpTeamCard>
        <MpTeamCard logo="src/lib/assets/marketplace-teams/spark-universe.jpg" team_name="Spark Universe" description="as a Freelancer"></MpTeamCard>
        <MpTeamCard logo="src/lib/assets/marketplace-teams/tinkrew.jpg" team_name="Tinkrew" description="as an Artist"></MpTeamCard>
        <MpTeamCard logo="src/lib/assets/marketplace-teams/eternal-creations.jpg" team_name="Eternal Creations" description="as an Artist"></MpTeamCard>
    </ul>
</section>

<h1>Active Projects</h1>
<ul>
    <button>Carnivore</button>
</ul>


<style>
    .about-me {
        margin-top: 4rem;

        display: grid;
        grid-template-columns: 1fr auto;
        grid-template-rows: 25rem;

        justify-items: left;

        position: relative;
    }

    .about-me > .text {
        margin-left: 1rem;
    }

    .about-me > .text > h1 {
        margin: 0;
        background-color: var(--primary-color-1);
        padding: 1rem;
    }

    .text {
        font-size: 1.3rem;
        text-align: justify;
    }

    .image-wrapper {
        position: relative;
    }

    .image-wrapper > img {
        height: 100%;
    }


    @media(max-width: 750px) {
        .about-me {
            margin-left: 1rem;
            margin-right: 1rem;
        }
        .text {
            font-size: 1rem;
            text-align: justify;
        }
        .image-wrapper > img {
            height: 60%;
        }

    }





    
    .previous-work {
        font-size: 1.3rem;
        margin-top: 4rem;
    }

    .previous-work > h1 {
        padding: 1rem;
        margin: 0;

        width: 50%;

        background-color: var(--primary-color-1);
    }

    .previous-work > .contractors {
        display: grid;
        grid-template-columns: 1fr 1fr;
        background-color: var(--neutral-color-1);
        border-radius: 0 1rem 1rem 1rem;
        margin-top: 0;
        padding: 1rem;
    }
</style>