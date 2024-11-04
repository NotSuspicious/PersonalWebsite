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
            title="SCARECROW"
            logo="/scarecrow/ScarecrowLogo.png"
            background="/scarecrow/ScarecrowBackground.jpg"
    />
    <div/>
    <div class='grid-container'>
        <div class="grid-item">
            <TextInsert text='
                    <strong>Scare-Crow</strong> is a humorous 3rd person stealth/planning game where you play as a crow who scares squirrels away from bird feeders.

                '/>
            <div class='grid-container-three'>
                <div class="grid-item">
                    <h3 class="roboto-condensed-bold-italic">ROLE</h3>
                    <ul class="roboto-regular">
                        <li>Technical Artist</li>
                    </ul>
                </div>
                <div class="grid-item">
                    <h3 class="roboto-condensed-bold-italic">TOOLS</h3>
                    <ul class="roboto-regular">
                        <li>Unity URP</li>
                        <li>HLSL</li>
                        <li>Shader Graph</li>
                        <li>Maya, Blender</li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <img class="image" src="/scarecrow/CG.jpg" alt="They Shall Not Come Back" />
        </div>
    </div>

    <div>
        <SectionHeader text= "Interactive Stylized Grass" />
        <TextInsert text='
            Created an interactive stylized grass system in <strong>Unity URP</strong>.
            <br>
            <br> - Used <strong>Shader Graph</strong> to design a wind effect and a procedural shading to achieve a cartoon look.
            <br> - Wrote custom Shader Graph nodes using <strong>HLSL</strong> to enable grass interaction.
            <br> - Created a custom <strong>URP Render Feature</strong> to convert game object data and exposed trample parameters into global shader variables.
            <br> - Scripted in <strong>C#</strong> to create components that could be attached to any game object to enable interactivity with grass.
            '/>

        <div class='grid-container'>
            <div class="grid-item">
                <a href="/scarecrow/GrassInteractionLogicFlow.png" target="_blank">
                    <img class="image" src="/scarecrow/GrassInteractionLogicFlow.png" alt="Grass Interaction Logic Flow" />
                </a>
            </div>
            <div class="grid-item">

                <iframe class="image" width="100%" height="300px" src="https://www.youtube.com/embed/FL5oUSqqkUc?si=A4kiY55J3BZyhZMs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
    </div>

    <div>
        <SectionHeader text= "Toon Shader & Post Processing" />
        <TextInsert text='
                - Developed a outline effect that uses <strong>ShaderGraph</strong> and a custom <strong>Render Pass</strong> to procedurally outline objects in the game based off normals.
                <br> - Created a <strong>toon-shader</strong> using Unity <strong>Shader Graph</strong>.
                <br> - Worked with Art Director, adjusting <strong>post-processing</strong> and <strong>lighting effects</strong> to achieve desired cartoon look.
            '/>

        <div class='grid-container'>
            <div class="grid-item">
                <img class="image" src="/scarecrow/NormalOutlines_Scarecrow.png" alt="They Shall Not Come Back" />
            </div>
            <div class="grid-item">
                <img class="image" src="/scarecrow/CelShader_scarecrow.png" alt="They Shall Not Come Back" />
            </div>
        </div>
    </div>



    <div>
        <SectionHeader text= "VFX"/>

        <div class='grid-container'>

            <div class="grid-item">
                <iframe class="image" width="100%" height="300px" src="https://www.youtube.com/embed/Zj8-eA_SZSg?si=5XGUPYl7OkJgmJj2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
            <div class="grid-item">
            </div>
        </div>
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