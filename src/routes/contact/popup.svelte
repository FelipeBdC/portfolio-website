<script lang="ts"> 
    import { get_current_component } from "svelte/internal";

    let lifetime = 2000;
    setTimeout(destroy, lifetime);

    const ThisComponent = get_current_component();


    function destroy() {
        ThisComponent.$destroy();
    }

</script>


<div class="popup popup-anim">
    <div class="popup-bg">
        <strong>Username Copied!</strong>
    </div>
</div>

<style>
    .popup {
        position: absolute;
        top: 0;
    }

    .popup > .popup-bg {
        text-align: center;
        color: black;
        background-color: white;
        border: 2px solid var(--neutral-color-0);
        border-radius: 1rem;

        padding: 1rem 0 1rem 0;
        width: 20ch;

    }

    .popup-anim {
        animation: pop 2000ms forwards;
    }

    @keyframes pop {
        0% {
            transform: translate(0, -100%);
        }

        30% {
            opacity: 1;
            transform: translate(0, 0);
        }

        80% {
            opacity: 1;
        }

        100% {
            opacity: 0;
        }
    }

</style>