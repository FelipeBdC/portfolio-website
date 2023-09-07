<script>
    import pop_gif from "$lib/assets/personal-work/pixel-art/pop.gif";
	import LetsWorkButton from "../components/buttons/lets-work-button.svelte";
    import arrow_down_icon from "$lib/assets/icons/arrow-down-s-line.svg";
	import LinkButton from "../components/buttons/link_button.svelte";
</script>



<header>
    <div class="background">
        <div class="overlay"></div>
    </div>

    <div class="wrapper">
        <section>
            <div class="text">
                <h1>Felipe de Souza</h1>
                <h2>welcome to my portfolio!</h2>
            </div>
            <nav>
                <LinkButton url="/contact" text="Let's Chat"></LinkButton>
                <LinkButton url="/about" text="About Me"></LinkButton>
            </nav>
        </section>
    </div>

    <div class="section-text">
        <img src={arrow_down_icon} alt="">
    </div>
    
</header>


<style>
    h1, h2 {
        margin: 0;
    }


    .background {
        position: absolute;

        background-image: url("src/lib/assets/personal-work/pixel-art/mockup-bar.png");
        background-size: cover;
        background-position: center;
        width: 100dvw;
        height: 100%;

        z-index: -1;
    }

    .overlay {
        width: 100%;
        height: 100%;
        background-color: var(--neutral-color-0);
        opacity: 40%;
    }


    header {
        display: flex;
        align-items: center;
        justify-content: center;

        height: 100dvh;
        position: relative;
    }

    .wrapper {
        display: flex;
        place-content: center;
        gap: 5rem;
    }
    .wrapper > img {
        width: 50%;
        place-self: center;
    }

    @media(max-width: 800px) {
        .wrapper {
            flex-wrap: wrap;
        }
        .wrapper > img {
            width: 80%;
        }
    }



    .section-text {
        display: flex;
        justify-content: center;
        gap: 0.2rem;
        margin-bottom: 2rem;
        padding: 1rem;

        position: absolute;
        bottom: 0;

    }
    .section-text > img {
        width: min(10vw, 3rem);
    }
    .section-text > h1 {
        font-size: min(6vw, 2rem);
        place-self: center;
        text-align: center;
    }



    .text {
        margin-bottom: 6rem;
        display: grid;
        place-content: center;
    }
    
    .text > h1 {
        font-size: min(10vw, 4rem);
        margin-bottom: 0.4ch;
    }
    .text > h2 {
        font-size: min(5vw, 1.5rem);
        text-align: center;
    }

    nav {
        display: flex;
        place-content: center;
        gap: min(4vw, 2rem);
    }

    a {
        all: unset;
        font-size: min(4vw, 1.2rem);
        place-self: center;
        cursor: pointer;
    }

</style>