<div class="buttons roboto-black-italic">
    <button on:click={() => window.open('https://www.linkedin.com', '_blank')}>LinkedIn</button>
    <button on:click={() => window.open('https://github.com', '_blank')}>GitHub</button>
    <button on:click={() => window.open('https://www.youtube.com', '_blank')}>YouTube</button>
    <button on:click={() => window.open('https://itch.io', '_blank')}>Itch.Io</button>
    <button on:click={() => window.open('https://www.example.com/resume.pdf', '_blank')}>Resume</button>
    <!-- <button>Email</button> -->
</div>

<style>
    .buttons {
        /* white-space: nowrap; */
        position: relative;
        padding: 0 0;
        margin-top: 28px;
        margin-left: -60px;
        width: calc(100% + 96px);

    }
    button {
        color: transparent;
        background-color: transparent;
        border: none;
        text-transform: uppercase;
        justify-content: flex-end; /* This will align the text to the right */
        align-items: flex-start; /* This will align the text to the top */
        text-align: left; /* This will align the text to the right */
        padding: 0;
        padding-top: 0px;
        font-size: 28pt;
        overflow: visible;
        margin: 8px 16px;
        position: relative;
        
    }
    .roboto-black-italic button{
        font-family: "Roboto Condensed", sans-serif;
        font-weight: 900;
        font-style: italic;
        color: var(--blue);
        text-transform: lowercase;
        text-shadow: 
            1px 1px 0 var(--white),
            -1px 1px 0 var(--white),
            -1px -1px 0 var(--white),
            1px -1px 0 var(--white);
    }

    button::before {
        content: '';
        background-color: var(--orange);
        position: absolute;
        bottom: -12px;
        width: calc(100%);
        height: 0px;
        transition: all .1s ease-in-out;
    }

    button:hover::before {
        height: 8px;
    }

    .roboto-black-italic button:hover {
        color: var(--white);
        text-shadow: none;
    }

    .roboto-condensed-black-italic {
        font-family: "Roboto Condensed", sans-serif;
        font-weight: 900;
        font-style: italic;
        color: var(--blue);
        transform: rotate(180deg);
        text-transform: lowercase;
        text-shadow: 
            1px 1px 0 var(--white),
            -1px 1px 0 var(--white),
            -1px -1px 0 var(--white),
            1px -1px 0 var(--white);
    }

    .roboto-condensed-black-italic:hover {
        color: var(--white);
        text-shadow: none;
    }
</style>