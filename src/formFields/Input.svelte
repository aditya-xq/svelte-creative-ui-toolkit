<script lang="ts">
    export let label: string;
    export let value: string;
</script>

<style src="Input.scss">
</style>

<div>
    <label for="input-a">{label}</label>
    <input type="text" id="input-a" bind:value={value}/>  
</div>