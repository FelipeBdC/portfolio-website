<script lang="ts">
    export let text: String = "";
</script>



<button class="see-more">{text}</button>


<style>
    .see-more {
        all: unset;
        padding: min(1.2vh, 1rem) min(4vw, 2rem) min(1.2vh, 1rem) min(4vw, 2rem);
        
        color: white;
        background-color: var(--neutral-color-15);
        z-index: 1;

        overflow: hidden;
        position: relative;
        
        cursor: pointer;
    }
    .see-more:hover, .see-more:focus {
        color: black;
        transition: 200ms ease-in;
    }

    .see-more::before {
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

    .see-more:hover::before, .see-more:focus::before {
        transform: translate(0, 0);
        transition: 200ms ease-in;
    }
</style>