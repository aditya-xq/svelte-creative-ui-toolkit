<script lang="ts">
    export let data: {parent: string, child: string}[];
</script>

<style src="Accordion.scss">
</style>

<div>
    <ul>
        {#each data as item}
        <li>
            <input type="checkbox" checked>
            <i></i>
            <h2>{item.parent}</h2>
            <p>{item.child}</p>
        </li>
        {/each}
    </ul>
</div>