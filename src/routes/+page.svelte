<script lang="ts">
    import "./+layout.css"
    import NavButton from "../components/buttons/nav-button.svelte";

    import PersonalTab from "./tabs/personal_tab.svelte";
    import ProfessionalTab from "./tabs/professional_tab.svelte";

    var tab_component = PersonalTab;

    var current_tab: string = "personal"

    function on_click(id: string) {
        current_tab = id
        check_tabs(id)
    }

    function check_tabs(id: string) {
        switch(id){
            case "personal": {
                console.log("personal!");
                tab_component = PersonalTab;
                break;
            }
            case "professional": {
                console.log("professional shit")
                tab_component = ProfessionalTab;
                break;
            }
        }
    }
</script>


<header>
    <h1>Hello</h1>
    <p>My name is Felipe, here's some of my work</p>
    <div class="ul-wrapper">
        <ul>
            <NavButton text="Personal" on_click={() => {on_click("personal")}} selected={current_tab == "personal"}></NavButton>
            <NavButton text="Professional" on_click={() => {on_click("professional")}} selected={current_tab == "professional"}></NavButton>
        </ul>
    </div>
</header>

<svelte:component this={tab_component}/>




<style>
    @import url('https://fonts.googleapis.com/css2?family=Freehand&display=swap');

    header {
        text-align: center;
        margin-bottom: 2rem;
        background-color: var(--color-60p);
        padding: 1rem;
        border-radius: 0 0 1ch 1ch;
    }
    header > h1 {
        font-family: 'Freehand', cursive;
        padding: 0;
        margin: 0;
        font-size: 4rem;
    }

    ul {
        display: flex;
        justify-content:center;
        padding: 0;
        gap: 2rem;
    }
</style>