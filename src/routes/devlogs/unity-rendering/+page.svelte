<script>
    import ProjectSplash from '../../ProjectSplash.svelte';
    import BackButton from '../../BackButton.svelte';
    import TextInsert from '../../TextInsert.svelte';
    import Button from '../../Button.svelte';
    import SectionHeader from '../../SectionHeader-small-long.svelte';
</script>

<body>
    <div class="content">
        <ProjectSplash
            title="Unity Rendering"
            logo="/unityurp/logo.png"
            background="/unityurp/background.png"
        />
        <div/>
        <div class='grid-container'>
            <div class="grid-item">
                <TextInsert text="
                    Over the summer of 2024, I learned a lot about Unity's <strong>Universal Render Pipeline</strong> (URP). I made this demo reel to show off some of the stuff I made!
                "/>
                <Button text="VIDEO LINK" className="button-large" link="https://youtu.be/EbQ-wMNsN5o?si=ihS0DPRXK70E0SSR"/>
            </div>
            <div class="grid-item">
                <iframe class="image" width="100%" height="300px" src="https://www.youtube.com/embed/EbQ-wMNsN5o?si=rqxTdx2uBXD4ZgHS" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>

        <div>

    </div>
</body>

<style>
    .content {
        padding: 72px;
        width: min(70%, 1080px);
        margin: auto;
        display: grid;
        gap: 24px;
    }

    .grid-container {
        display: grid;
        grid-template-columns: repeat(2, 1fr); /* Two equal columns */
    }

    .grid-container-three {
        display: grid;
        grid-template-columns: repeat(3, 1fr); /* Two equal columns */
        gap: 12px;
    }

    .grid-item {
        /* Default styles for grid items */
    }

    a {
        color: var(--white); /* Example link color */
        text-decoration: none;
        position: relative;
        padding: 8px 0px;
        font-size: 24px; /* Adjust font size as needed */
    }

    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 32px;
        margin: 20px 0;
    }
</style>