<div class="sidebar roboto-condensed-black-italic">
    <a href="/" class="element">Home</a>
    <a href="/fun" class="element">Fun</a>
    <a href="/music" class="element">Music</a>
</div>

<style>
    .sidebar {
        width: 108px;
        height: 80vh;
        position: fixed;
        right: 0;
        top: 0;
    }

    .element {
        writing-mode: vertical-rl;
        margin: 60px 0px;
        font-size: 60px;
        border: none;

        color: var(--blue);
        transform: rotate(180deg);
        text-transform: lowercase;
        text-shadow: 
            1px 1px 0 var(--white),
            -1px 1px 0 var(--white),
            -1px -1px 0 var(--white),
            1px -1px 0 var(--white);
    }

    .element::before {
        content: '';
        background-color: var(--orange);
        position: absolute;
        left: 0;
        bottom: 0;
        width: 0px;
        height: 100%;
        transition: all .1s ease-in-out;
    }

    .element:hover::before {
        width: 8px;
    }

    .element:hover {
        color: var(--white);
        text-shadow: none;
    }
</style>