<script lang="ts">
    let count = 0;
</script>

<button type="button" on:click={() => (count += 1)} class="btn btn-primary"
    >Testing1</button
>
<button type="button" on:click={() => (count += 1)} class="btn btn-success"
    >Testing2</button
>
