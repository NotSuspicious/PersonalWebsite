<script>
    export let title = '';
    export let href = '';
</script>

<a href={href} class="sidebar roboto-condensed-black-italic">
    {title}
</a>

<style>
    .sidebar {
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

    .sidebar::before {
        content: '';
        background-color: var(--orange);
        position: absolute;
        left: 0;
        bottom: 0;
        width: 0px;
        height: 100%;
        transition: all .1s ease-in-out;
    }

    .sidebar:hover::before {
        width: 8px;
    }

    .sidebar:hover {
        color: var(--white);
        text-shadow: none;
    }
</style>