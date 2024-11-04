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
        position: relative;
        box-shadow: 5px 5px 0 white;
        transition: box-shadow 0.1s;
    }

    .back-button:hover {
        box-shadow: 0 0 0 var(--white);
    }
</style>

<button class="back-button roboto-condensed-medium-italic" on:click={goBack}>
    GO Back
</button>