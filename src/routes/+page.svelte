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
    import SidebarElement from './SidebarElement.svelte';
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
        
        <div class="content">
            
            <SectionHeader text="FEATURED WORKS" />

            <Project 
                title="VR Gameplay Engineer"
                img=""
                tags={['Unreal Engine 5', 'Blender', 'Logic Pro', 'Meta Quest 3']}
            />
            <Project 
                title="Engineer"
                img=""
                tags={['Unreal Engine 5', 'Blender', 'Logic Pro', 'Meta Quest 3']}
            />
            <Project 
                title="Director"
                img=""
                tags={['Unreal Engine 5', 'Blender', 'Logic Pro', 'Meta Quest 3']}
            />
        </div>
        
        <img src="/Footer.svg" alt="Footer" />
        
        
        <div class="sidebar">
            <SidebarElement title="Home"/>
            <SidebarElement title="Fun"/>
            <SidebarElement title="Music"/>
        </div>
        
   
</body>

<style>
     :root {
        --blue: #358BAF;
        --orange: #C17F1C;
        --white: #FFFFFF;
        --highlight: #F2BC6B;
    }

    html, body {
        /* padding: calc(8px + 1.5625vw);
        margin-left: 4vw;
        margin-right: 8vw; */
        margin: 0;
        padding: 0;
        background-color: var(--blue);
        overflow-x: hidden;
    }

    .sidebar {
        width: 108px;
        height: 80vh;
        position: fixed;
        right: 0;
        top: 0;
    }



    model-viewer {
        /* margin: max(calc(1200px - vw), 0) 0; */
        
        width: 600px;
        height: 100%;
        /* margin-left: -200px; */
        
    }

    .header {
        margin: 48px 0;
    }

    .header-img {
        width: 550px;
        height: auto;
    }
    
    .landing-page {
        display: grid;
        height: min(1080px, 100vh);
        width: min(70%, 1080px);
        grid-template-columns: 50% 50%;
        grid-template-rows: 1fr;
        margin-top: 32px;
        margin: auto;   
    }
    

    @media (max-width: 992px) { /* This will apply the styles inside the braces when the window is narrower than 600px */
        .landing-page {
            grid-template-columns: 1fr;
            grid-template-rows: 1fr 1fr;
            margin: 0 10vw;
        }
    }

    .content {
        color: var(--white);
        font-family: "Roboto", sans-serif;
        font-weight: 400;
        font-style: italic;
        font-size: 20px;
        line-height: 1.5;
        width: min(84%, 1400px);
        margin: auto;
        border: 1px solid var(--white);
    }

    img {
        width: 100%;
        height: auto;
        pointer-events: none; /* This will disable pointer events for the images */
        user-select: none; /* This will disable user selection for the images */
    }

</style>
