<script>
    import pop_gif from "$lib/assets/personal-work/pixel-art/pop.gif";
	import LetsWorkButton from "../components/buttons/lets-work-button.svelte";
    import arrow_down_icon from "$lib/assets/icons/arrow-down-s-line.svg";
</script>



<header>
    <div class="wrapper">
        <section>
            <div class="text">
                <h1>Felipe de Souza, 18</h1>
                <h2><i>&gt i can bring your ideas to life</i></h2>
            </div>
            <nav>
                <LetsWorkButton></LetsWorkButton>
                <a href="/about">About Me</a>
            </nav>
        </section>
        <img src={pop_gif} alt="">
    </div>

    <div class="section-text">
        <img src={arrow_down_icon} alt="">
        <h1>My Work</h1>
    </div>
    
</header>


<style>
    h1, h2 {
        margin: 0;
    }

    header {
        display: flex;
        align-items: center;
        justify-content: center;

        height: 100svh;
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
        border-left: 2px solid white;
        padding: 1rem;
        padding-left: 1rem;
        margin-bottom: 2rem;
    }
    
    .text > h1 {
        font-size: min(8vw, 3rem);
        margin-bottom: 1rem;
    }
    .text > h2 {
        font-size: min(4vw, 1.5rem);
    }

    nav {
        display: flex;
        gap: min(4vw, 2rem);
    }

    a {
        all: unset;
        font-size: min(4vw, 1.2rem);
        place-self: center;
        cursor: pointer;
    }

</style>