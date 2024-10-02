<script>
    export let text = ''; // Prop for the button text
    export let link = '#'; // Prop for the button link
    export let className = ''; // Prop for additional class names
</script>

<button class="button roboto-condensed-medium-italic {className}" on:click={() => window.open(link, '_blank', 'noopener noreferrer')}>
    {text}
</button>

<style>
    :global(.button) {
        color: var(--white); /* Example link color */
        text-decoration: none;
        position: relative;
        padding: 8px 0px;
        font-size: 24px; /* Default font size */
        display: inline-block;
        background: none; /* Remove default button background */
        border: none; /* Remove default button border */
        cursor: pointer; /* Change cursor to pointer */
        outline: none; /* Remove default button outline */
    }

    :global(.button)::before {
        content: '';
        background-color: var(--orange);
        position: absolute;
        bottom: 0; /* Position the line at the bottom of the link */
        left: 0;
        width: 100%;
        height: 0px; /* Initial height of the line */
        transform-origin: bottom right; /* Start the animation from the right */
        transition: height 0.1s ease-in-out; /* Smooth transition */
    }

    :global(.button:hover)::before {
        height: 6px;
    }
</style>