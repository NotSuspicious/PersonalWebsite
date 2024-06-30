<script>
    import Sidebar from './Sidebar.svelte';
</script>

<div class="page-container">
    <Sidebar/>

    <div class="content-wrap">
        <slot/>
    </div>

    <img src="/Footer.svg" alt="Footer" class="footer" />
</div>

<style>
    .page-container {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
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