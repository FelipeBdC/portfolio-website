<script lang="ts">
    export var text: String = "Button";
    export var selected: boolean = false;
    export var on_click = () => {};
</script>


<button class:selected="{selected}" on:click={on_click}>{text}</button>

<style>
    button {
        all: unset;
        cursor: pointer;
        min-width: 12ch;
        text-align: center;        
        padding: 1ch;

        border: 0.2rem solid;
        border-color: var(--color-30p);
        border-radius: 2ch;

        transition: 150ms;

        color: white;
    }
    button:hover {
        color: black;
        background-color: white;
        border-color: white;
    }

    .selected {
        color: black;
        background-color: var(--color-10p);
        border-color: var(--color-10p);
    }
    .selected:hover {
        background-color: var(--color-10p);
        border-color: var(--color-10p);
    }
</style>