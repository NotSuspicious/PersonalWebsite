<head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Condensed:ital,wght@0,100..900;1,100..900&amp;family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&amp;display=swap" rel="stylesheet" />
</head>

<script>
    import Navbar from "./Navbar.svelte"; 
</script>

<body class="page-container">
    <Navbar/>

    <div class="content-wrap">
        <slot/>
    </div>

    <img src="/Footer.svg" alt="Footer" class="footer" />
</body>

<style global>
    .page-container {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }

    :global(strong) {
        color: var(--highlight);
        text-transform: uppercase;
        font-style: italic;
        letter-spacing: 0px;
        font-family: "Roboto", sans-serif;
    }

    .content-wrap {
        flex: 1 0 auto; /* This will make the content wrap grow if there's space available */
    }

    .footer {
        flex-shrink: 0; /* This will prevent the footer from shrinking */
        width: 100%;
        height: auto;
        pointer-events: none; /* This will disable pointer events for the images */
        user-select: none; /* This will disable user selection for the images */
    }

    :global(a) {
        text-decoration: none; /* This will remove the underline from all links */
    }

    :global(.roboto-condensed-regular-italic) {
        font-family: "Roboto Condensed", sans-serif;
        font-weight: 400;
        font-style: italic;
    }

    :global(.roboto-condensed-medium-italic) {
        font-family: "Roboto Condensed", sans-serif;
        font-weight: 500;
        font-style: italic;
    }

    :global(.roboto-condensed-bold-italic) {
        font-family: "Roboto Condensed", sans-serif;
        font-weight: 600;
        font-style: italic;
    }

    :global(.roboto-condensed-black-italic) {
        font-family: "Roboto Condensed", sans-serif;
        font-weight: 900;
        font-style: italic;
    }

    :global(.roboto-regular) {
        font-family: "Roboto", sans-serif;
        font-weight: 400;
        letter-spacing: 0.25px;
    }
    :root {
        --blue: #358BAF;
        /* --orange: #d48d21; */
        --orange: #C17F1C;
        --white: #FFFFFF;
        --highlight: #F2BC6B;
    }

    :global(body) {
        margin: 0;
        padding: 0;
        background-color: var(--blue);
        overflow-x: hidden;
    }
    
</style>