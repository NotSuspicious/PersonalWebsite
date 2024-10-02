<script>
    export let text = '';
</script>
  
<h2 class="header roboto-condensed-medium-italic">
    <span class="underline">{text}</span>
</h2>

<style>


.header {
    width: 100%;
    margin: 0;
    padding: 24px 0 0 0;
}

.underline {
    position: relative;
}
.underline::after {
    content: '';
    position: absolute;
    left: 0;
    bottom: 6px; /* Adjust underline distance */
    height: 6px; /* Adjust thickness */
    width: 100%;
    background-color: var(--orange); /* Adjust color */
}

h2 {
    color: var(--white);
    font-size: 36pt;
    white-space: nowrap;
}
</style>