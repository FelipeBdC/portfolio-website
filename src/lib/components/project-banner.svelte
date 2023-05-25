<script lang="ts">
    export let src: string = "";
    export let title: string = "";
    export let description: string = "";

    let img_src = new URL("../" + src, import.meta.url).href;


    
</script>

<div class="banner" style="--background-image: url('{img_src}');">
    <div class="color-layer"></div>
    <div class="text">
        <h1>{title}</h1>
        <p>{description}</p>
    </div>
</div>

<style>
    .banner {
        width: 100%;
        height: 40ch;

        position: relative;
        background-image: var(--background-image);
        background-position: top;
        background-size: 100%;
        background-size: cover;

        border-radius: var(--default-border-radius);
        overflow: hidden;

        display: flex;
        flex-direction: column;
        justify-content: end;
        align-items: center;
    }
    .banner > .color-layer {
        position: absolute;
        background: linear-gradient(#00000000 40%, #000000 100%);
        width: 100%;
        height: 100%;
    }
    .banner > .text {
        z-index: 1;
        text-align: center;
        margin: 2ch;
    }
    .banner > .text > * {
        margin: 1ch;
    }

    @media(max-width: 800px) {
        .banner {
            background-position: center;
        }
    }
</style>