<script lang="ts">
    import xp_logo from "$lib/assets/marketplace-teams/xp-games.jpg";
    import tinkrew_logo from "$lib/assets/marketplace-teams/tinkrew.jpg";
    import eternal_logo from "$lib/assets/marketplace-teams/eternal-creations.jpg";
    import spark_logo from "$lib/assets/marketplace-teams/spark-universe.jpg";
    import MpTeamCard from "../../components/cards/mp-team-card.svelte";
</script>


<h1>Teams i worked with</h1>
<div class="recent-teams">
    <MpTeamCard team_name="XP Games" description="Artist" logo={xp_logo}></MpTeamCard>
    <MpTeamCard team_name="Spark Universe" description="Artist(Freelancer)" logo={spark_logo}></MpTeamCard>
    <MpTeamCard team_name="Eternal Creations" description="Artist" logo={eternal_logo}></MpTeamCard>
    <MpTeamCard team_name="Tinkrew" description="Artist" logo={tinkrew_logo}></MpTeamCard>
</div>



<style>
    .recent-teams {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-auto-flow: row;

        overflow: hidden;

        gap: 1rem;
        border-radius: 1rem;
    }
</style>
