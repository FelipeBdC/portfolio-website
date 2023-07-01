
<script>
    import bar_pixelart from "$lib/assets/personal-work/pixel-art/mockup-bar.png";

    import discord_logo from "$lib/assets/icons/discord-mark-white.svg";
    import twitter_logo from "$lib/assets/icons/icons8-twitter.svg";

	import LinkButton from "../../components/buttons/link_button.svelte";
    import Popup from "./popup.svelte";

    function copy_discord() {
        show_popup()
        navigator.clipboard.writeText("felipebdc")
    }

    function show_popup() {
        const popup = new Popup({target: document.querySelector('#popup-container')})
    }

</script>

<header>
    <div id="popup-container"></div>
    <img src={bar_pixelart} alt="">
    <h1 class="big-text">Services</h1>
</header>

<main>
    <section>
        <div class="medium-text">
            <strong>Want me to join your team?</strong>
        </div>
        <div class="centered">
            <div class="small-text">Unavailable</div>
        </div>
    </section>
    <section>
        <div class="medium-text">
            <strong>Commissions</strong>
        </div>
        <div class="centered">
            <div class="small-text">Send me a DM!</div>
            <div class="socials">
                <button class="logo-button" on:mousedown={copy_discord}><img src={discord_logo} alt="Discord"></button>
                <a href="https://twitter.com/felipe_does_pxl" target="_blank" class="logo-button"><img src={twitter_logo} alt="Twitter"></a>
            </div>
        </div>
    </section>
</main>

<footer>
    <LinkButton text="Return" url="/"></LinkButton>
</footer>


<style>


    


    #popup-container {
        position: relative;
        width: 100%;
        display: flex;
        justify-content: center;
    }


    header {
        margin-top: min(2vh, 1rem);
        max-width: 100%;
    }

    header > img {
        width: 100%;
        max-height: 40dvh;
        object-fit: cover;
        object-position: top;
        padding: 0.4rem;
        border: 2px solid var(--neutral-color-1);

        box-sizing: border-box;
    }

    h1 {
        text-align: center;
        margin: min(4vh, 4rem);
    }

    .centered {
        display: flex;
        flex-direction: column;
        place-content: center;
        height: 100%;
    }



    main {
        display: grid;
        grid-auto-flow: column;
        grid-auto-columns: 1fr;
        gap: min(2vh, 2rem);
    }

    section {
        padding: 2vh 1.5rem 2vh 1.5rem;

        text-align: center;
        border: 2px solid var(--neutral-color-1);
        transition: 500ms ease-out;
    }
    section:hover {
        border-color: var(--neutral-color-2);
        transition: 200ms ease-in;
    }

    section > .big-text {
        width: 100%;
    }

    

    .socials {
        display: flex;
        place-content: center;
        margin-top: 1rem;
        gap: 4ch;
    }

    .socials > button {
        all: unset;
    }

    .logo-button > img {
        width: min(10vw, 6ch);
        transition: 200ms;
    }

    .logo-button> img:hover {
        transform: scale(105%);
    }





    footer {
        margin-top: 2rem;
        display: flex;
    }

    @media(max-width: 700px) {
        footer {
            display: flex;
            justify-content: center;
        }

        main {
            grid-auto-flow: row;
            grid-auto-rows: 1fr 1fr;
        }
    }
</style>