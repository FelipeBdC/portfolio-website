<script lang="ts">
	import { afterNavigate } from '$app/navigation';
    import { page, navigating } from '$app/stores';

    let current_route: string = $page.url.pathname;
    export let logo: string = new URL("$lib/assets/picture_felipe.jpg", import.meta.url).href;

    afterNavigate(() => {current_route = $page.url.pathname;})


</script>

<header>
    <div class="header-content">
        <img src={logo} alt="Felipe">
        <nav class="horizontal-nav">
            <ul>
                <li><a href="/" class="link nav-button {current_route == "/" ? "selected" : "unselected"}">Home</a></li>
                <li><a href="/my-work" class="link nav-button {current_route == "/my-work" ? "selected" : "unselected"}">My Work</a></li>
                <li><a href="/about" class="link nav-button {current_route == "/about" ? "selected" : "unselected"}">About</a></li>
                <li><a href="/contact" class="link nav-button {current_route == "/contact" ? "selected" : "unselected"}">Contact </a></li>
            </ul>
        </nav>
    </div>
</header>


<style>
    header {
        width: 100%;

        background: var(--color-background1);
        border-radius: var(--default-border-radius);
    }
    .header-content {
        display: flex;
        align-items: center;
        justify-content:space-between;
        gap: 4rem;
        padding: 2rem;
    }
    .header-content > img {
        --img-scale: 8ch;
        width: var(--img-scale);
        height: var(--img-scale);

        border-radius: 50%;
        border: 3px solid var(--color-highlight0);
        padding: 6px;
    }
    .horizontal-nav {
        display: none;
    }
    @media(min-width: 800px) {
        .horizontal-nav {
            display: block;
        }
    }
    @media(max-width: 600px) {
        .header-content {
            padding-left: 1rem;
            padding-right: 1rem;
            justify-content: space-between;
        }
        .header-content > img {
            --img-scale: 20%
        }
    }

    .horizontal-nav > ul {
        display: flex;
        gap: 1rem;

        padding: 0;
        list-style: none;

        min-width: 10ch;
    }
    .nav-button {
        transition: 400ms;
        border-bottom: 2px solid #00000000;
        padding: 1ch;
    }
    .unselected:hover {
        transform: scale(1.05);
        transition: 200ms;
        border-bottom: 4px solid var(--color-highlight1);
    }
    .selected {
        transition: 0ms;
        border-bottom: 4px solid var(--color-highlight0);
    }

    .link {
        text-decoration: none;
        color: white;
    }
</style>