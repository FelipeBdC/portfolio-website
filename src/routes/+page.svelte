<script lang="ts">
    import "./+layout.css";
    import MinecraftTab from "./tabs/minecraft-tab.svelte";
    import PixelArtTab from "./tabs/pixel-art-tab.svelte";
	import MarketplaceTab from "./tabs/marketplace-tab.svelte";
	import NavButton from "../components/buttons/nav-button.svelte";

    var tab_component = MinecraftTab;
    var current_tab: string = "minecraft";

    function on_click(id: string) {
        current_tab = id
        check_tabs(current_tab)
    }

    function check_tabs(id: string) {
        switch(id){
            case "minecraft": {
                tab_component = MinecraftTab;
                console.log("minecraft");
                break;
            }
            case "marketplace": {
                tab_component = MarketplaceTab;
                console.log("marketplace");
                break;
            }
            case "pixelart": {
                tab_component = PixelArtTab;
                console.log("pixelart");
                break;
            }
        }
    }
</script>


<nav>
    <ul>
        <NavButton text="Minecraft" on_click={() => {on_click("minecraft")}} selected={current_tab=="minecraft"}></NavButton>
        <NavButton text="Marketplace" on_click={() => {on_click("marketplace")}} selected={current_tab=="marketplace"}></NavButton>
        <NavButton text="Pixel Art" on_click={() => {on_click("pixelart")}} selected={current_tab=="pixelart"}></NavButton>
    </ul>
</nav>

<svelte:component this={tab_component}/>



<style>
    nav {
        margin: 2rem 10rem 2rem 10rem;
    }

    nav > ul {
        padding: 0;
        display: grid;
        grid-auto-flow: column;
        gap: 1rem;
    }
</style>