<script>
    export let text = '';
</script>
  
<h2 class="roboto-black-italic">
    <span class="underline">{text}</span>
</h2>

<style>
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

.roboto-black-italic {
    font-family: "Roboto Condensed", sans-serif;
    font-weight: 900;
    font-style: italic;
    color: var(--white);
    font-size: 72pt;
    white-space: nowrap;
}
</style>