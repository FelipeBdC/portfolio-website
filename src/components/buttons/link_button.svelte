<script lang="ts">
    export let text: string = "";
    export let url: string = "";
</script>



<a class="medium-text" href={url}>{text}</a>


<style>
    a {
        all: unset;
        padding: min(1.2vh, 1rem) min(4vw, 2rem) min(1.2vh, 1rem) min(4vw, 2rem);
        
        color: white;
        border: 0.2ch solid white;
        z-index: 1;
        overflow: hidden;
        position: relative;
        cursor: pointer;

        display: flex;
        width: 8ch;
        justify-content: center;
        transition: 200ms ease-out;
    }
    a:hover, a:focus {
        color: black;
        border-color: white;
        background-color: white;
        transition: 200ms ease-in;
    }
    

    
</style>