<script lang="ts">
    export let link: string;
    export let text: string;
    export let id: string;
    export let style: string;
</script>

<style src="Link.scss">
</style>

<div {id} class="link-container">
    <a class={['link', style].filter(Boolean).join('-')} href={link}>{text}</a>
</div>