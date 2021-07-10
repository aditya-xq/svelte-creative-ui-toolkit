<script>
    export let link='';
    export let text='';
</script>

<!-- styling based on https://codepen.io/jhancock532/pen/GRZrLwY -->

<style type="text/scss">
    .link-container {
        display: inline-flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100%;
        position: relative;
        z-index: 0;
    }

    .link-three {
        color: #eb7132;
        font-size: 30px;
        margin: 5ch;
    }

    .link-three::after {
        content: "";
        position: absolute;
        z-index: 2;
        width: 50%;
        height: 100%;
        top: 0%;
        left: 0%;
        transform: translate(0, -50%) scaleY(0);
        transition: transform 1s ease;
        mix-blend-mode: difference;

        clip-path: polygon(
            20% 60%,
            100% 60%,
            100% 40%,
            20% 40%,
            20% 0%,
            60% 0%,
            60% 20%,
            20% 20%
        );
        background-color: #eb7132;
    }

    .link-three:hover::after {
        transform: translate(0, 0%) scaleY(1);
    }

    .link-three::before {
        content: "";
        position: absolute;
        z-index: 2;
        width: 50%;
        height: 100%;
        bottom: 0%;
        right: 0%;
        transform: translate(0, 50%) scaleY(0);
        transition: transform 1s ease;
        mix-blend-mode: difference;

        clip-path: polygon(
            80% 40%,
            0% 40%,
            0% 60%,
            80% 60%,
            80% 100%,
            40% 100%,
            40% 80%,
            80% 80%
        );
        background-color: #eb7132;
    }

    .link-three:hover::before {
        transform: translate(0%, 0%) scaleY(1);
    }
</style>

<div class="link-container">
    <a class="link-three" href={link}>{text}</a>
</div>