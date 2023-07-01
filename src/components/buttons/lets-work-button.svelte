<div class="button-wrapper">
    <div class="button-slide-wrapper">
        <a href="/contact">Lets Chat</a>
    </div>
</div>

<style>
    .button-wrapper {
        display: grid;
        place-content: start;


        font-size: min(4vw, 1.2rem);
    }

    .button-wrapper > .button-slide-wrapper {
        width: fit-content;
    }

    .button-slide-wrapper > a {

        --border-radius: 0.5rem;

        all: unset;
        position: relative;
        z-index: 1;

        color: white;

        border: 2px solid white;

        padding: min(1.5vh, 1rem) min(8vw, 2rem) min(1.5vh, 1rem) min(8vw, 2rem);
        transition: 100ms;
        cursor: pointer;

        overflow: hidden;
    }

    .button-slide-wrapper > a:hover, a:focus {
        color: black;
        transition: 100ms;
    }

    .button-slide-wrapper > a::before {
        z-index: -1;
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: white;
        width: 0;
        transform-origin: left;
        transition: 150ms;

    }

    .button-slide-wrapper > a:hover::before, a:focus::before {
        width: 100%;
    }

</style>