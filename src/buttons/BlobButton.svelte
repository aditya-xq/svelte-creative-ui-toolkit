<script lang="ts">
    export let buttonText: string;
    export let onClick;
</script>

<style src="Button.scss">
</style>

<button
    on:click={onClick}
    class="blob-btn"
>
    {buttonText}
    <span class="blob-btn__inner">
        <span class="blob-btn__blobs">
            <span class="blob-btn__blob"></span>
            <span class="blob-btn__blob"></span>
            <span class="blob-btn__blob"></span>
            <span class="blob-btn__blob"></span>
        </span>
    </span>
</button>

<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
    <defs>
        <filter id="goo">
        <feGaussianBlur in="SourceGraphic" result="blur" stdDeviation="10"></feGaussianBlur>
        <feColorMatrix in="blur" mode="matrix" values="1 0 0 0 0 0 1 0 0 0 0 0 1 0 0 0 0 0 21 -7" result="goo"></feColorMatrix>
        <feBlend in2="goo" in="SourceGraphic" result="mix"></feBlend>
        </filter>
    </defs>
</svg>