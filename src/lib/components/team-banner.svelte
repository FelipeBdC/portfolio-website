<script lang="ts">
    export let bg_src: string = "";
    export let logo_src: string = "";
    export let name: string = "";
    export let role: string = "";

    let background_url = new URL("../" + bg_src, import.meta.url).href;
    let logo_url = new URL("../" + logo_src, import.meta.url).href;


    
</script>

<div class="banner" style="--background-image: url('{background_url}');">
    <div class="color-layer"></div>
    <img src={logo_url} alt="">
    <div class="text">
        <h1>{name}</h1>
        <p>{role}</p>
    </div>
</div>

<style>
    .banner {
        width: 100%;
        height: 30ch;

        position: relative;
        background-image: var(--background-image);
        background-position: top;
        background-size: 100%;
        background-size: cover;

        border-radius: var(--default-border-radius);
        overflow: hidden;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .banner > .color-layer {
        position: absolute;
        background: linear-gradient(#00000000 20%, #000000 100%);
        width: 100%;
        height: 100%;
    }
    .banner > .text {
        z-index: 1;
        text-align: center;
        font-size: small;
    }
    .text > h1, p{
        margin: 0;
    }
    .text > p {
        font-size: medium;
        margin-top: 1ch;
    }
    img {
        z-index: 1;
        width: 8ch;
        border-radius: var(--default-border-radius);
        border: 4px solid white;
        margin-bottom: 1ch;
    }

    @media(max-width: 800px) {
        .banner {
            background-position: center;
        }
    }
</style>