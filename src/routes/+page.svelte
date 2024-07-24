

<script>
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
                    'I’m William, a <strong>Game Developer</strong>, <strong>TECHNICAL ARTIST</strong>, and a <strong>MUSICIAN</strong>. I’m studying computer science @ USC Games.
                    <br/>
                    <br/>
                    My greatest passion is leveraging my technical and creative skills to create multimedia experiences.
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
            <SectionHeader text="FEATURED WORKS" />
            <Project 
            title="They Shall Not Come Back"
            role="VR Gameplay Engineer"
            background="/images/TSNCB-Background.png"
            logo="/images/TSNCB-Logo.png"
            tags={['Unreal Engine 5', 'Blender', 'Logic Pro', 'Meta Quest 3']}
            blogName="they-shall-not-come-back"
            />
            <Project 
            title="Computational Fluid Dynamics"
            role="Engineer"
            background="/images/CFD-Background.png"
            logo="/images/CFD-Logo.png"
            tags={['Unreal Engine 5', 'Blender', 'Logic Pro', 'Meta Quest 3']}
            blogName="computational-fluid-dynamics"
            />
            <Project 
            title="Rat Pack"
            role="Director"
            background="/images/RatPack-Background.png"
            logo="/images/RatPack-Logo.png"
            tags={['Unreal Engine 5', 'Blender', 'Logic Pro', 'Meta Quest 3']}
            blogName="ratpack"
            />
        </div>
</body>

<style>
    model-viewer {
        width: 600px;
        height: 100%;
    }
    
    .landing-page {
        display: grid;
        height: min(1080px, 100vh);
        width: min(70%, 1080px);
        grid-template-columns: 50% 50%;
        grid-template-rows: 1fr;
        margin: auto;   
    }
    
    .header {
        margin: 48px 0;
    }

    .header-img {
        width: 550px;
        height: auto;
    }

    @media (max-width: 992px) { /* This will apply the styles inside the braces when the window is narrower than 600px */
        .landing-page {
            grid-template-columns: 1fr;
            grid-template-rows: 1fr 1fr;
            margin: 0 10vw;
        }
    }

    .content {
        width: min(70%, 1080px);
        margin: auto;
    }

    img {
        width: 100%;
        height: auto;
        pointer-events: none; /* This will disable pointer events for the images */
        user-select: none; /* This will disable user selection for the images */
    }

</style>
