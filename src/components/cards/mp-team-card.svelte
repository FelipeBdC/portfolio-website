<script lang="ts">
    export var logo: string = "";
    export var team_name: string = "Team";
    export var description: string = "Description";

    var info_open: boolean = false;

    function open_info() {
        info_open = true;
    }
    function close_info() {
        info_open = false;
    }
</script>


<div class="team-card" on:mouseenter={open_info} on:mouseleave={close_info}>
    <img src={logo} alt="{team_name} Logo">
    <div class="info {info_open == true ? '' : 'invisible'}">
        <h3><strong>{team_name}</strong></h3>
        <p><i>{description}</i></p>
    </div>
</div>

<style>

    .team-card {
        display: grid;
        grid-auto-flow: column;
        grid-template-columns: 10rem;
        grid-template-rows: 10rem;;

        background-color: var(--color-60p);
        
        padding: 1rem;
        border-radius: 1rem;
        transition: 400ms;

        place-self: center;
    }

    .team-card:hover {
        background-color: var(--color-30p);
    }

    .team-card > img {
        height: 100%;
        width: 100%;
        margin: 0;
        border-radius: 1rem;
    }

    .info {
        width: 15ch;
        text-align: start;
        transition: 300ms;
        margin-left: 1rem;
        white-space: nowrap;
    }

    .invisible {
        margin: 0;
        width: 0;
        color: transparent;
    }
</style>