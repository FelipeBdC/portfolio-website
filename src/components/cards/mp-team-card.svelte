<script lang="ts">
    export var src: any;
    export var team_name: string = "Team";
    export var description: string = "Description";
</script>


<div class="team-card">
    <img src={src} alt="{team_name} Logo">
    <div class="info">
        <h2><strong>{team_name},</strong></h2>
        <p>{description}</p>
    </div>
</div>

<style>

    .team-card {
        color: white;
        text-align: start;

        display: grid;
        grid-auto-flow: column;
        grid-template-columns: 5rem;
        grid-template-rows: 5rem;
        gap: 1rem;

        
        padding: 1rem;
        border-radius: 1rem;
        transition: 400ms;

    }

    .team-card > img {
        height: 100%;
        width: 100%;
        margin: 0;
        border-radius: 1rem;
    }

    .info > p {
        margin: 0;
        font-size: large;
    }

    .info > h2 {
        margin: 0;
    }

</style>