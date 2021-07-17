<script lang="ts">
    export let style: string;
</script>

<style src="Button.scss">
</style>

<div class="btn-toggle">
    <span class={'switcher ' + ['switcher', style].filter(Boolean).join('-')}>
        <input type="checkbox" id="switcher">
        <label for="switcher"></label>
    </span>
</div>