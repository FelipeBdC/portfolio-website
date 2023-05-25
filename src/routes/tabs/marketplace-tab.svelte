<script lang="ts">
    import xp_logo from "$lib/assets/marketplace-teams/xp-games.jpg";
    import tinkrew_logo from "$lib/assets/marketplace-teams/tinkrew.jpg";
    import eternal_logo from "$lib/assets/marketplace-teams/eternal-creations.jpg";
    import spark_logo from "$lib/assets/marketplace-teams/spark-universe.jpg";
    import MpTeamCard from "../../components/cards/mp-team-card.svelte";
</script>


<div class="recent-teams"> 
    <h1>Who I Worked With</h1>
    <div class="team-list">
        <MpTeamCard team_name="XP Games - Current" description="Artist" logo={xp_logo}></MpTeamCard>
        <MpTeamCard team_name="Spark Universe" description="Artist(Freelancer)" logo={spark_logo}></MpTeamCard>
        <MpTeamCard team_name="Eternal Creations" description="Artist" logo={eternal_logo}></MpTeamCard>
        <MpTeamCard team_name="Tinkrew" description="Artist" logo={tinkrew_logo}></MpTeamCard>
    </div>
</div>

<h1>Products</h1>



<style>
    .recent-teams {
        padding-top: 0.1rem;
        border-radius: 1rem;
        background-image: linear-gradient(to bottom, var(--color-10p) 20%, var(--color-10p-shade) 25%);
        color: var(--color-60p);
    }

    .recent-teams > h1 {
        margin-left: 2rem;
    }

    .team-list {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-auto-flow: row;

        background-color: var(--color-30p);
        overflow: hidden;

        gap: 0.5rem;
        border-radius: 1rem;

        padding: 1rem;
    }
</style>
