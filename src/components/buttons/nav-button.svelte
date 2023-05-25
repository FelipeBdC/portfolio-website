<script lang="ts">
    export var text: String = "Button";
    export var selected: boolean = false;
    export var on_click = () => {};
</script>


<button class:selected="{selected}" on:click={on_click}>{text}</button>

<style>
    button {
        color: red;

        all: unset;
        cursor: pointer;
        min-width: 12ch;
        text-align: center;        
        border: var(--color-30p) solid 2px;
        padding: 1ch;
        border-radius: 2ch;
        transition: 200ms;
    }
    button:hover {
        background-color: var(--color-30p);
    }

    .selected {
        border-color: var(--color-10p);
        background-color: var(--color-10p);
        color: black;
    }
    .selected:hover {
        border-color: var(--color-10p);
        background-color: var(--color-10p);
    }
</style>