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
            title="UE5 Top Down Prototype"
            logo=""
            background="/topdown/blog-background.jpg"
    />
    <div class='grid-container'>
        <div class="grid-item">
            <TextInsert text="
                     A top-down game with a variety of gameplay systems I wrote primarily in <strong>C++</strong>:
                    Logic gates, interactables, physics-based puzzles, dashing and proning, and AI stealth, vision, and patrolling.
                "/>
            <Button text="VIDEO LINK" className="button-large" link="https://www.youtube.com/watch?v=6ZD80bfXHhM"/>
        </div>
        <div class="grid-item">
            <iframe class="image" width="100%" height="300px" src="https://www.youtube.com/embed/6ZD80bfXHhM?si=7Yi3Kx2Fww3XCyP8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        </div>
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