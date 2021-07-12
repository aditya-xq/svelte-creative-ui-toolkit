<script lang="ts">
    export let buttonText: string;
    export let onClick;
    export let style: string;
</script>

<style src="Button.scss">
</style>

<button
    on:click={onClick}
    class={['btn', style].filter(Boolean).join('-')}>{buttonText}
</button>