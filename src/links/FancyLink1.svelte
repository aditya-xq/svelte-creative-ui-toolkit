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

    .link-one {
        color: #53d9d1;
        transition: color 1s cubic-bezier(0.32, 0, 0.67, 0);
        margin: 5ch;
        font-size: 30px;
    }

    .link-one:hover {
        color: #111;
        transition: color 1s cubic-bezier(0.33, 1, 0.68, 1);
    }

    .link-one::before {
        content: "";
        position: absolute;
        z-index: -1;
        width: 100%;
        height: 100%;
        top: 0;
        right: 0;
        background-color: #53d9d1;

        clip-path: circle(0% at 50% calc(50%));
        transition: clip-path 1s cubic-bezier(0.65, 0, 0.35, 1);
    }

    .link-one:hover::before {
        clip-path: circle(100% at 50% 50%);
    }

    .link-one::after {
        content: "";
        position: absolute;
        z-index: -1;
        width: 100%;
        height: 100%;
        top: 0;
        right: 0;
        background-color: #151515;

        clip-path: polygon(
            40% 0%,
            60% 0%,
            60% 0%,
            40% 0%,
            40% 100%,
            60% 100%,
            60% 100%,
            40% 100%
        );
        transition: clip-path 1s cubic-bezier(0.65, 0, 0.35, 1);
    }

    .link-one:hover::after {
        clip-path: polygon(
            40% 10%,
            60% 10%,
            60% 35%,
            40% 35%,
            40% 90%,
            60% 90%,
            60% 65%,
            40% 65%
        );
    }
</style>

<div class="link-container">
    <a class="link-one" href={link}>{text}</a>
</div>