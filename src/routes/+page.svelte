<head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Condensed:ital,wght@0,100..900;1,100..900&amp;family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&amp;display=swap" rel="stylesheet" />
</head>

<script>
    import Project from './Project.svelte';
    import SectionHeader from './SectionHeader.svelte';
    import TextInsert from './TextInsert.svelte';
    import ButtonRow from './ButtonRow.svelte';
    import List from './List.svelte';
</script>
  
<body>
    
        <div class="landing-page">
            <div class="landing-page-column">
                <div class="header"><img class="header-img" src="/WilliamZhao.svg" alt="William Zhao" /></div>
                <TextInsert/>
                <ButtonRow/>
            </div>
            
            <div class="landing-page-column">
                <model-viewer id="reveal" loading="eager" src="/models/WilliamIdle.glb" camera-controls disable-zoom poster="/models/poster.webp" autoplay/>     
            </div>
        </div>
        
        <SectionHeader text="SKILLS" />
        <div>
            <List></List>
        </div>

        <SectionHeader text="FEATURED WORKS" />
        <div class="content">
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
        width: min(55%, 1300px);
        margin: auto;
    }

    img {
        width: 100%;
        height: auto;
        pointer-events: none; /* This will disable pointer events for the images */
        user-select: none; /* This will disable user selection for the images */
    }

</style>
