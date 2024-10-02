

<script>
    import LargeProject from './LargeProject.svelte';
    import Project from './Project.svelte';
    import SectionHeader from './SectionHeader.svelte';
    import SectionHeaderSmall from './SectionHeader-small.svelte';
    import TextInsert from './TextInsert.svelte';
    import ButtonRow from './ButtonRow.svelte';
    import List from './List.svelte';
</script>
  
<body>
        <div class="landing-page">
            <div class="landing-page-column">
                <div class="header"><img class="header-img" src="/WilliamZhao.svg" alt="William Zhao" /></div>
                <TextInsert text=
                    'I’m William, a <strong>Game Engineer</strong> with a love for <strong>TECHNICAL ART</strong>. I’m currently studying computer science @ USC Games.
                    <br/>
                    <br/>
                    My greatest passion is leveraging my technical and creative skills to create polished and visually stunning games.
                    <br/>
                    <br/>
                    Whether that be through <strong>PC GAMES</strong>, <strong>VR EXPERIENCES</strong>, or <strong>PHYSICS SIMULATIONS</strong>, you can always catch me working on something I love!'    
                />
                <ButtonRow/>
            </div>
            
            <div class="landing-page-column">
                <model-viewer id="reveal" loading="eager" src="/models/WilliamIdle.glb" camera-controls disable-zoom poster="/models/poster.webp" autoplay/>     
            </div>
        </div>

        <div class="content">
            <SectionHeaderSmall text="SKILLS" />
            <List/>
            <div id="projects"> <SectionHeader text="PROJECTS" /> </div>
            
            <LargeProject 
            title="They Shall Not Come Back"
            role="VR Gameplay Engineer"
            background="/images/TSNCB-Background.png"
            logo="/images/TSNCB-Logo.png"
            award="/images/TSNCB-Award.png"
            tags={['Unreal Engine 5', 'Blender', 'Logic Pro', 'Meta Quest 3']}
            blogName="they-shall-not-come-back"
            />

            <div class="project-grid">
                <LargeProject 
                title="Computational Fluid Dynamics"
                role="Engineer"
                background="/cfd/background.png"
                logo="/cfd/logo.png"
                blogName="computational-fluid-dynamics"
                />
                <LargeProject 
                title="Unity Rendering"
                role="Technical Artist"
                background="/unityurp/background.png"
                logo="/unityurp/logo.png"
                blogName="unity-rendering"
                />
                <!-- <LargeProject 
                title="Scarecrow"
                role="Technical Artist"
                background="/images/RatPack-Background.png"
                logo=""
                blogName="scarecrow"
                />
                <LargeProject 
                title="Iron Testament"
                role="Technical Artist"
                background="/images/RatPack-Background.png"
                logo=""
                blogName="rateconomy"
                /> -->
                <!-- <LargeProject 
                title="DONUTS!"
                role="Technical Artist"
                background="/images/RatPack-Background.png"
                logo=""
                blogName="ratpack"
                /> -->
                
            </div>
            
        </div>
</body>

<style>
    model-viewer {
        width: 100%;
        height: 100%;
        align-items: right;
    }
    
    .landing-page {
        display: grid;
        width: min(70%, 1080px);
        grid-template-columns: 50% 50%;
        grid-template-rows: 1fr;
        margin: auto;   
        gap: 24px;
        padding-bottom: 100px;
    }
    
    .header {
        margin: 48px 0;
    }

    .header-img {
        width: 550px;
        height: auto;
    }

    @media (max-width: 992px) {
        .landing-page {
            grid-template-columns: 1fr;
            grid-template-rows: 1fr 1fr;
            margin: 0 10vw;
        }

        .project-grid {
            grid-template-columns: 1fr; /* Change to a single column */
            gap: 24px 0; /* Adjust gap for single column layout */
        }
    }

    .content {
        width: min(70%, 1080px);
        margin: auto;
        padding-bottom: 100px;
    }

    .project-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 0px 72px;
    }

    img {
        width: 100%;
        height: auto;
        pointer-events: none; /* This will disable pointer events for the images */
        user-select: none; /* This will disable user selection for the images */
    }

</style>
