<script lang="ts">
    export let text: string = "";
    export let url: string = "";
</script>



<a href={url}>{text}</a>


<style>
    a {
        all: unset;
        padding: min(1.2vh, 1rem) min(4vw, 2rem) min(1.2vh, 1rem) min(4vw, 2rem);
        
        color: white;
        border: 2px solid var(--neutral-color-2);
        z-index: 1;
        overflow: hidden;
        position: relative;
        cursor: pointer;

        display: flex;
        width: 8ch;
        justify-content: center;
        transition: 400ms ease-out;
    }
    a:hover, a:focus {
        color: black;
        border-color: white;
        background-color: white;
        transition: 400ms;
    }

    a::before {
        backface-visibility: hidden;

        z-index: -1;
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: white;
        transform-origin: left;
        transform: translate(-110%, 0);
        transition: 200ms ease-out;

        width: 120%;
    }

    
</style>