<script>
    import {get} from "svelte/store";
    import {page} from "$app/stores";

    let from = get(page).url.searchParams.get("from");
</script>

<h3>Login</h3>
{#if from}
<p>
    You came from {from}
</p>
{:else}
<p>
    TODO: login form
</p>
{/if}