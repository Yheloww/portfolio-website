<script>
    export let data

    import { fly,fade } from "svelte/transition";
</script>

{#key data.pathname}
<div in:fly={{ y: -50, duration: 300, delay:350}}>
    <slot/>
</div>
{/key}