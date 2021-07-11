<script>
    export let link = '';
    export let text = '';
    export let id = null;
    export let style = '';
</script>

<style src="Link.scss">
</style>

<div {id} class="link-container">
    <a class={['link', style].filter(Boolean).join('-')} href={link}>{text}</a>
</div>