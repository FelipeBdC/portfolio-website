
<main>
    <div class="text">
        <h1>Welcome to the Pixel Art page!<br></h1>
        <p>...which doesn't exist rn :/ <br>take a cup of coffee instead ☕</p>
        <a href="/"><strong>Take Coffee And Go Back ☕</strong></a>
    </div>
</main>



<style>
    main {
        display: grid;
        place-items: center;
        text-align: center;
        width: 100%;
        height: 100%;
    }

    .text {
        display: grid;
        align-items: center;

        background-color: var(--neutral-color-1);
        padding: 1rem;
        border-radius: 1rem;
        height: 15rem;
    }

    a {
        all: unset;
        
        color: var(--neutral-color-0);
        background-color: var(--secondary-color-2);
        padding: 1rem;
        margin: 2rem;
        
        border-radius: 1rem;

        transition: 100ms ease-in;
    }

    a:hover {
        background-color: var(--primary-color-2);
        transition: 200ms ease-out;
    }
</style>