<script>
    export let buttonText = '';
    export let onClick;
    export let style = '';
</script>

<style src="Button.scss">
</style>

<button
    on:click={onClick}
    class={'btn ' + ['btn', style].filter(Boolean).join('-')}>{buttonText}
</button>