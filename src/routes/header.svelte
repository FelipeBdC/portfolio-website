<script>
    import picture_felipe from "$lib/assets/picture-felipe.jpg";
	import LetsWorkButton from "../components/buttons/lets-work-button.svelte";
	import NavButton from "../components/buttons/nav-button.svelte";
</script>

<header>
    <section id="section1">
        <div class="image-wrapper">
            <img src={picture_felipe} alt="Felipe">
        </div>
        <div class="greeting">
            <h3>&#62; <i>Hi, my name is</i></h3>
            <h1>Felipe de Souza, 18</h1>
            <p><i>Asset creator, Game Developer<br>and Front-End developer.</i></p>
            <LetsWorkButton></LetsWorkButton>
        </div>
        
    </section>
</header>

<style>
    header {
        display: grid;
        grid-template-columns: auto;
        grid-auto-flow: column;
        gap: 1rem;

        background-color: var(--neutral-color-1);
        border-radius: 0 0 10rem 1rem;
        padding: 2rem;
    }

    header > #section1 {
        display: grid;
        grid-auto-flow: column;
        grid-template-rows: 15rem;
        width: fit-content;
    }

    #section1 > .image-wrapper {
        background-color: var(--secondary-color-1);
        border-radius: 1rem;
        height: 100%;
    }

    .image-wrapper > img {
        transform: translate(0.5rem, -0.5rem);
        height: 100%;
        border-radius: 1rem;
    }



    .greeting {
        display: flex;
        flex-direction: column;

        margin: 1ch;
        margin-left: 1.5rem;
        padding: 1rem;
        border-left: 0.3rem solid white;
    }

    .greeting > h3, h1 {
        margin: 0;
    }
    .greeting > h1 {
        font-size: xx-large;
    }


    #section2 {
        background-color: var(--primary-color-1);
        padding: 1rem;

        display: flex;
        flex-direction: column;
        position: relative
    }

    #section2 > ul {
        padding: 0;
        margin: 0;
    }

    #section2 > h2 {
        margin: 0;
        margin-bottom: 1ch;
    }

    @media (max-width: 750px) {
        header {
            padding: 1rem;
        }

        header > #section1 {
            grid-template-rows: 12rem;
        }

        .greeting {
            margin-top: 0;
            padding-top: 0;
            display: block;
            height: min-content;
        }
        .greeting > h1 {
            font-size: x-large;
        }

        .greeting > p {
            font-size: medium;
        }

    }
</style>