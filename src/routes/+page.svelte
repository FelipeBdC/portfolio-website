<script lang="ts">
	import Header from "./header.svelte";
	import ThingsIDo from "./things-i-do.svelte";

    var age = 18;

</script>


<main>
    <Header></Header>
    <ThingsIDo></ThingsIDo>
</main>


<style>
    main {
        display: flex;
        flex-direction: column;

        place-items: center;
        justify-content: center;
        height: 100%;
        gap: 3rem;

        margin: 0 8rem 0 8rem;
    }



    @media(max-width: 1100px) {
        main {
            margin: 1rem;
        }
    }

    @media(max-width: 300px) {
        main {
            margin: 0;
        }
    }

</style>