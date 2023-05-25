<script lang="ts">
    export let src: string = "";
    export let txt: string = "";
    export let selected: boolean = false;

    let img_src = "../" + src
</script>


<button class="category {selected ? "selected" : "unselected"}">
    <img src={new URL(img_src, import.meta.url).href} alt={txt}>
    <p><strong>{txt}</strong></p>
</button>

<style>
    .category {
        color: white;
        background: var(--color-highlight0);

        --size: 25ch;

        max-width: var(--size);
        max-height: var(--size);
        width: var(--size);
        height: var(--size);

        padding: 4ch;
        border: none;
        border-radius: var(--default-border-radius);

        cursor: pointer;
        transition: 800ms;
    }
    .category > img {
        width: 50%;
        margin-bottom: 2ch;
    }
    .category > p {
        margin: 0;
        font-size: medium;
        max-width: 100%;
    }
    @media(max-width: 900px) {
        .category {
            --size: 100%;
            padding: 2ch;
        }
    }
    @media(max-width: 400px) {
        .category {
            display: flex;
            flex-direction: row-reverse;
            column-gap: 1rem;
            justify-content: center;
            align-items: center;
        }
        .category > img {
            width: 30%;
            margin-bottom: 0;
        }
        .category > p {
            width: 70%;
            text-align: start;
        }
    }

    .selected {
        background-color: var(--color-highlight1);
    }
    .unselected:hover {
        background: var(--color-highlight2);
        transition: 200ms;
    }
</style>