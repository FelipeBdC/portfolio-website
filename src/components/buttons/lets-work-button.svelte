<div class="button-wrapper">
    <div class="button-slide-wrapper">
        <button><strong>Let's Chat!</strong></button>
    </div>
</div>

<style>
    .button-wrapper {
        display: grid;
        place-content: end;
        width: 100%;
        margin-top: 4rem;
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

    @media(max-width: 700px) {
        .button-wrapper {
            margin: 0;
        }

        .button-slide-wrapper > button {
            padding: 0.5rem 1rem 0.5rem 1rem;
        }
        
        button > strong {
            font-size: small;
        }
    }

</style>