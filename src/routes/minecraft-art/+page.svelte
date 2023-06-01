<script lang="ts">

    import velociraptor_gif from "$lib/assets/personal-work/minecraft/velociraptor.gif";

    import couch_image from "$lib/assets/personal-work/minecraft/couch.png";
    import chair_image from "$lib/assets/personal-work/minecraft/chair.png";
    import stool_image from "$lib/assets/personal-work/minecraft/stool.png";

    import sorcerers_cloak from "$lib/assets/personal-work/minecraft/sorcerers-cloak.gif";
    import mechanic_suit from "$lib/assets/personal-work/minecraft/mechanic-suit.gif";
    import lightning_cloak from "$lib/assets/personal-work/minecraft/lightning-cloak.gif";
    import fire_hoodie from "$lib/assets/personal-work/minecraft/fire-hoodie.gif";

</script>



<main>
    
    <header>
        <div class="text">
            <h2>My mission is to</h2>
            <h1 class="highlight-strong">Take <strong>your ideas</strong> out of the paper</h1>
        </div>
        <div class="image-wrapper">
            <img src={velociraptor_gif} alt="Velociraptor">
        </div>
        <svg id="svg1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" fill="var(--neutral-color-1)"></path></svg>
        <svg id="svg2" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" fill="var(--neutral-color-1)"></path></svg>

    </header>

    <section class="showcase-section">
        <h1 class="left-border highlight-strong">As <strong>simple</strong> as they are</h1>
        <div class="image-grid-wrapper">
            <div class="image-grid">
                <img src={couch_image} alt="">
                <img src={chair_image} alt="">
                <img src={stool_image} alt="">
            </div>
        </div>
    </section>
    
    <section class="showcase-section">
        <h1 class="right-border highlight-strong">Or as <strong>legendary</strong> as they can be</h1>
        <div class="image-grid-wrapper">
            <div class="image-grid">
                <img src={sorcerers_cloak} alt="">
                <img src={mechanic_suit} alt="">
                <img src={lightning_cloak} alt="">
                <img src={fire_hoodie} alt="">
            </div>
        </div>
    </section>
    <img src="" alt="">


</main>


<style>
    :global(body) {
        height: 100%;
    }


    header {
        display: grid;
        grid-auto-flow: column;
        grid-template-columns: 1fr 1fr;
        font-size: 1.5rem;

        position: relative;

        gap: 4rem;
    }

    header > svg {
        z-index: -1;
        position: absolute;
        scale: 50%;
    }

    header > #svg1 {
        transform: translate(30%, -40%);
    }

    header > #svg2 {
        scale: 40%;
        transform: translate(-70%, 30%);
    }

    .text {
        background-color: var(--primary-color-1);
        padding: 1rem;
        padding-top: 6rem;
        border-radius: 1rem 1rem 14rem 1rem;
    }

    h1, h2 {
        margin: 0;
    }

    .highlight-strong > strong {
        color: var(--secondary-color-2);
    }

    .image-wrapper {
        display: flex;
        justify-content: center;
    }

    .image-wrapper > img {
        height: auto;
        width: 100%;
    }


    section {
        font-size: 1.8rem;    
        margin-bottom: 4rem;  
    }

    section > h1 {
        margin-top: 4rem;
        margin-bottom: 4rem;
        height: min-content;
    }

    .right-border {
        border-radius: 0 0 14rem 0;
    }

    .left-border {
        border-radius: 0 0 0 14rem;
        text-align: right;
    }


    .image-grid-wrapper {
        background-color: var(--secondary-color-1);
        border-radius: 1rem;
        max-width: 100%;
        margin-right: 0.5rem;
    }

    .image-grid {
        background-color: var(--neutral-color-2);
        display: grid;
        grid-auto-flow: column;
        padding: 2rem;
        border-radius: 1rem;
        transform: translate(0.5rem,-0.5rem);
    }

    .image-grid > img {
        place-self: center;
        
        width: 100%;
        height: auto;
    }
</style>