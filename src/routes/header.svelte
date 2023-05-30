<script>
    import picture_felipe from "$lib/assets/picture-felipe.jpg";
	import LetsWorkButton from "../components/buttons/lets-work-button.svelte";
</script>

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

<style>
    header {
        display: grid;
        grid-auto-flow: column;
        place-items: start;
        position: relative;
        width: 100%;

        grid-template-columns: 1.5fr 2fr;
    }

    header > svg {
        z-index: -1;
        position: absolute;
        transform: translate(0, -60%);
        scale: 50%;
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

    .text {
        font-size: large;
        display: grid;
        grid-template-rows: 1fr 1fr;
        width: 100%;
    }

    .text > h1, p {
        margin: 0 0 0 0;
        padding-left: 1rem;
    }

    .text > h1 {
        background-color: var(--primary-color-1);
        border-radius: 0 4rem 0 0;

        margin-bottom: 1rem;
        padding: 0.5rem 2rem 0.5rem 2rem;
        
        display: flex;
        align-items: center;
    }



    @media(max-width: 700px) {
        .text > h1 {
            font-size: large;
            padding: 0.5rem 0 0.5rem 1rem;
        }

        .text > p {
            font-size: small;
        }
    }


    @media(max-width: 300px) {
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
    }
</style>