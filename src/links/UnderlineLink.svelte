<script>
    export let text = '';
    export let link = '';
</script>

<!-- Styling is based on https://codepen.io/alphardex/pen/NWxNyXb-->

<style type="text/scss">
    @import '../../global';
    .menu-nav-link {
        display: inline-flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100%;
        position: relative;
        font-size: 2rem;
        color: $color-text;
        text-decoration: none;

        span {
            overflow: hidden;
            div {
                transform: translateY(102%);
            }
        }

        &::after {
            position: absolute;
            content: "";
            top: 100%;
            left: 0;
            width: 100%;
            height: 3px;
            background: $color-highlighted;
            transform: scaleX(0);
            transform-origin: right;
            transition: transform 0.5s;
        }

        &:hover::after {
            transform: scaleX(1);
            transform-origin: left;
        }
    }
</style>

<a class="menu-nav-link" href={link}>
    <span>{text}</span>
</a>