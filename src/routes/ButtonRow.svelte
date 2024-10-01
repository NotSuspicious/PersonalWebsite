<div class="buttons">
    <button class="roboto-condensed-black-italic" on:click={() => window.open('https://www.linkedin.com/in/williamzhaodesign/', '_blank')}>LinkedIn</button>
    <button class="roboto-condensed-black-italic" on:click={() => window.open('https://github.com/NotSuspicious', '_blank')}>GitHub</button>
    <button class="roboto-condensed-black-italic" on:click={() => window.open('https://www.youtube.com/@WilliamZhao', '_blank')}>YouTube</button>
    <button class="roboto-condensed-black-italic" on:click={() => window.open('mailto:williezhao123@gmail.com', '_blank')}>Email</button>
    <button class="roboto-condensed-black-italic" on:click={() => window.open('https://drive.google.com/file/d/15OCYBA9wQRsYm-zb0yh-L8WzpNuRZpOe/view?usp=sharing', '_blank')}>Resume</button>
    <button class="roboto-condensed-black-italic" on:click={() => window.open('https://qwer2999.itch.io/', '_blank')}>Itch.Io</button>
    <!-- <button>Email</button> -->
</div>

<style>
    .buttons {
        /* white-space: nowrap; */
        position: relative;
        padding: 0 0;
        margin-top: 28px;
        margin-left: 0px;
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
        cursor: pointer; /* This will change the cursor to a pointer when hovering over buttons */

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
        bottom: -10px;
        width: calc(100%);
        height: 0px;
        transition: all .1s ease-in-out;
    }

    button:hover::before {
        height: 8px;
    }

    button:hover {
        color: var(--white);
        text-shadow: none;
    }

</style>