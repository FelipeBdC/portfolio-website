<script lang="ts">
    export var href: string = "";
</script>


<a href={href}><slot/></a>

<style>
    a {
        all: unset;
        padding: 0.5rem 0 0.5rem 1rem;
        text-align: left;
        border-radius: 1rem;
        transition: 200ms ease-in;
        cursor: pointer;
        font-size: large;
    }

    a:hover {
        background-color: var(--neutral-color-2);
        padding-left: 1.5rem;

    }
    
    @media(max-width: 700px) {
        a {
            font-size: small;
            padding: 0.2rem 0 0.2rem 0.5rem;
        }
    }
</style>