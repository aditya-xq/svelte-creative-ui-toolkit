<script>
    export let link='';
    export let text='';
</script>

<!-- styling based on https://codepen.io/jhancock532/pen/GRZrLwY -->

<style type="text/scss">
    @import '../../global';
    .link-container {
        display: inline-flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100%;
        position: relative;
        z-index: 0;
    }

    .link-two {
        color: #f27b9b;
        transition: color 1s cubic-bezier(0.32, 0, 0.67, 0);
        font-size: 30px;
        margin: 5ch;
    }

    .link-two:hover {
        color: #111;
        transition: color 1s cubic-bezier(0.33, 1, 0.68, 1);
    }

    .link-two::before {
        content: "";
        position: absolute;
        z-index: -2;
        width: 100%;
        height: 100%;
        top: 0;
        right: 0;
        clip-path: polygon(
            0% -20%,
            100% -30%,
            100% -10%,
            0% 0%,
            0% 130%,
            100% 120%,
            100% 100%,
            0% 110%
        );
        background-color: #f27b9b;
        transition: clip-path 1s cubic-bezier(0.25, 1, 0.5, 1);
    }

    .link-two:hover::before {
        clip-path: polygon(
            0% 10%,
            100% 0%,
            100% 20%,
            0% 30%,
            0% 100%,
            100% 90%,
            100% 70%,
            0% 80%
        );
    }

    .link-two::after {
        content: "";
        position: absolute;
        z-index: -1;
        width: 5ch;
        height: 5ch;
        top: 50%;
        right: 50%;
        transform: translate(50%, -50%) rotate(0deg) scale(0);
        transition: transform 1s ease;
        background-color: #f27b9b;
    }

    .link-two:hover::after {
        transform: translate(50%, -50%) rotate(135deg) scale(1);
    }
</style>

<div class="link-container">
    <a class="link-two" href={link}>{text}</a>
</div>