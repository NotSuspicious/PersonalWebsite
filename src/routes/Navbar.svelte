<nav class="navbar roboto-condensed-medium-italic">
    <div class="navbar-left">
        <span class="brand">William's Portfolio</span>
    </div>
    <div class="navbar-right">
        <a href="/#projects">Projects</a>
    </div>
</nav>

<style>
    .navbar {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: min(80%, 1200px);
        margin: auto;
        padding: 24px 0px;
        color: white; /* Example text color */
    }

    .navbar-left {
        flex: 1;
    }

    .navbar-right {
        display: flex;
        gap: 72px; /* Adjust gap between links as needed */
    }

    .brand {
        font-size: 32px; /* Adjust font size as needed */
    }

    a {
        color: var(--white); /* Example link color */
        text-decoration: none;
        position: relative;
        padding: 8px 0px;
        font-size: 32px; /* Adjust font size as needed */
    }

    a:hover {
       
    }
    a::before {
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

    a:hover::before {
        height: 6px;
    }
</style>