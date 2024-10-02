<script>
    function goBack() {
        history.back();
    }
</script>

<style>
    .back-button {
        display: inline-block;
        padding: 4px 24px;
        font-size: 32px;
        color: var(--white);
        background-color: var(--orange);
        border: none;
        cursor: pointer;
        text-transform: uppercase;
    }

</style>

<button class="back-button roboto-condensed-medium-italic" on:click={goBack}>
    GO Back
</button>