<script lang="ts">
    export var href: string = "";
    export var icon: any; // fuck you ts users
</script>


<a href={href}><img src={icon} alt="Icon"></a>

<style>
    a {
        all: unset;
        padding: 0.5rem 1rem 0.5rem 1rem;
        border-radius: 1rem;

        width: 14ch;

        background-color: var(--secondary-color-2);
        color: black;

        display: grid;
        place-items: center;

    }

    a > img {
        width: 6ch;
        height: 6ch;
    }

    a:hover, a:focus {
        background-color: var(--primary-color-2);
        color: white;
    }


</style>