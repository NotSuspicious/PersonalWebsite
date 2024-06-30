<script>
    export let text = '';
</script>
  
<h2 class="header roboto-condensed-black-italic">
    <span class="underline">{text}</span>
</h2>

<style>


.header {
    width: min(70%, 1080px);
    margin: auto;
}

.underline {
    position: relative;
}
.underline::after {
    content: '';
    position: absolute;
    left: 0;
    bottom: 12px; /* Adjust underline distance */
    height: 12px; /* Adjust thickness */
    width: 100%;
    background-color: var(--orange); /* Adjust color */
}

h2 {
    color: var(--white);
    font-size: 72pt;
    white-space: nowrap;
}
</style>