<script>
    export let text = '';
</script>
  
<h2 class="header roboto-condensed-black-italic">
    <span class="underline">{text}</span>
</h2>

<style>


.header {
    width: 100%;
    margin: auto;
    padding-bottom: 48px;
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

@media (max-width: 580px)
{
    h2 {
        font-size: 32pt;
    }
    .underline::after {
        left: 0;
        bottom: 5px; /* Adjust underline distance */
        height: 6px; /* Adjust thickness */
        width: 100%;
    }
}
</style>