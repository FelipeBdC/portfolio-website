<div class="button-wrapper">
    <div class="button-slide-wrapper">
        <button><strong>Let's Work Together!</strong></button>
    </div>
</div>

<style>
    .button-wrapper {
        display: flex;
        flex-direction: column;
        flex-grow: 1;
        justify-content: flex-end;
    }

    .button-wrapper > .button-slide-wrapper {
        width: fit-content;
    }

    .button-slide-wrapper > button {
        all: unset;
        position: relative;
        z-index: 1;


        color: var(--neutral-color-0);
        background-color: var(--secondary-color-2);

        border-radius: 0.5rem;

        padding: 1rem;
        text-align: center;
        transition: 100ms;
        cursor: pointer;
    }

    .button-slide-wrapper > button:hover, button:focus {
        color: white;
        transition: 100ms;
    }

    .button-slide-wrapper > button::before {
        z-index: -1;
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: var(--primary-color-1);
        border-radius: 0.5rem;
        transform: scaleX(0);
        transform-origin: center;
        transition: transform 100ms;

    }

    .button-slide-wrapper > button:hover::before, button:focus::before {
        transform: scaleX(1);
    }
</style>