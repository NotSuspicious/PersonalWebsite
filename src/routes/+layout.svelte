<head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Condensed:ital,wght@0,100..900;1,100..900&amp;family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&amp;display=swap" rel="stylesheet" />

   	<!-- HTML Meta Tags -->
<title>William Zhao's Portfolio</title>
<meta name="description" content="I’m William, a Game Engineer with a love for Technical Art. I’m currently studying computer science @ USC Games.

    ">

<!-- Facebook Meta Tags -->
<meta property="og:url" content="https://www.williamz.design">
<meta property="og:type" content="website">
<meta property="og:title" content="William Zhao's Portfolio">
<meta property="og:description" content="I’m William, a Game Engineer with a love for Technical Art. I’m currently studying computer science @ USC Games.

    ">
<meta property="og:image" content="https://opengraph.b-cdn.net/production/images/039fc191-a484-4f0a-8b11-3a6f206200ce.png?token=8j_87Xnycw4omjonMQPAljjJHn4TiTmqcPSsEujDV30&height=667&width=1200&expires=33263898503">

<!-- Twitter Meta Tags -->
<meta name="twitter:card" content="summary_large_image">
<meta property="twitter:domain" content="williamz.design">
<meta property="twitter:url" content="https://www.williamz.design">
<meta name="twitter:title" content="William Zhao's Portfolio">
<meta name="twitter:description" content="I’m William, a Game Engineer with a love for Technical Art. I’m currently studying computer science @ USC Games.

    ">
<meta name="twitter:image" content="https://opengraph.b-cdn.net/production/images/039fc191-a484-4f0a-8b11-3a6f206200ce.png?token=8j_87Xnycw4omjonMQPAljjJHn4TiTmqcPSsEujDV30&height=667&width=1200&expires=33263898503">

<!-- Meta Tags Generated via https://www.opengraph.xyz -->
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

    :global(.roboto-bold) {
        font-family: "Roboto", sans-serif;
        font-weight: 700;
        letter-spacing: 0.25px;
    }

    :global(h3) {
        font-size: 22pt;
        color: var(--highlight);
        white-space: nowrap;
        margin: 0 0 6px 
    }
    :global(ul) {
        list-style-type: none;
        padding: 0;
        margin: 0;
        color: var(--white);
        font-size: 14pt;
    }

    :global(li) {
        margin: 0 0 2px 0;
    }

    :global(button) {
        color: var(--white); /* Example link color */
        text-decoration: none;
        position: relative;
        padding: 8px 0px;
        font-size: 24px; /* Adjust font size as needed */
        display: inline-block;
        background-color: transparent;
        border: none;
        cursor: pointer;
    }

    :global(button)::before {
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

    :global(button:hover)::before {
        height: 6px;
    }

    :global(.button-large) {
        font-size: 32px; /* Larger font size */
    }

    :global(.button-small) {
        font-size: 24px; /* Smaller font size */
    }

    :global(.image) {
        width: 100%;
        height: 300px;
        object-fit: cover; /* Ensure the image fills the container while maintaining aspect ratio */
        box-shadow: 8px 8px var(--orange); /* Orange drop shadow */
        transition: box-shadow 0.1s ease-in-out;
    }

    :global(.image)::hover {
        box-shadow: 12px 12px var(--orange);
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