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
            title="They Shall Not Come Back"
            award="/images/TSNCB-Award.png"
            logo="/images/TSNCB-Logo.png"
            background="/images/TSNCB-Background.png"
        />
        <div/>
        <div class='grid-container'>
            <div class="grid-item">
                <TextInsert text='
                    <strong>THEY SHALL NOT COME BACK</strong> is a narrative-driven VR interactive experience where you play the lingering soul of a teenage soldier who is killed in WWI. Scroll down to learn more about my role and the tools I used!
                '/>
                <div class='grid-container-three'>
                    <div class="grid-item">
                        <Button text="TRAILER" className="button-large" link="https://vimeo.com/994876347?autoplay=1&muted=1&stream_id=Y2xpcHN8MTQ3NzIxNjQwfGlkOmRlc2N8W10%3D"/>
                        <Button text="LEARN MORE" className="button-large" link="https://www.selenyxie.com/tsnc-presskit"/>
                    </div>
                    <div class="grid-item">
                        <h3 class="roboto-condensed-bold-italic">ROLES</h3>
                        <ul class="roboto-regular">
                            <li>VR Gameplay Engineer</li>
                        </ul>
                    </div>
                    <div class="grid-item">
                        <h3 class="roboto-condensed-bold-italic">TOOLS</h3>
                        <ul class="roboto-regular">
                            <li>Unreal Engine 5</li>
                            <li>Blender</li>
                            <li>Logic Pro</li>
                            <li>Meta Quest 3</li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="grid-item">
                <img class="image" src="/tsncb/ShortClip.webp" alt="They Shall Not Come Back" />
            </div>
        </div>

        <div>
            <SectionHeader text= "VR Interactable Piano" />
            <TextInsert text='
            Developed an interactable piano with physics-based VR controls in <strong>Unreal Engine 5</strong>.
            <br><br> - Used <strong>Blueprinting</strong> to prototype interaction, audio, and haptic feedback.
            <br> - Used <strong>Material Editor</strong> to create shaders for the final look. (Left Image)
            <br> - Used <strong>Logic Pro</strong> to create the piano audio.
            '/>
        
            <div class='grid-container'>
                <div class="grid-item">
                    <img class="image" src="/tsncb/Piano.webp" alt="They Shall Not Come Back" />
                </div>
                <div class="grid-item">
                    
                    <iframe class="image" width="100%" height="300px" src="https://www.youtube.com/embed/5U1Q_yJjo3c?si=CI5iSiLXPquGLJiu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </div>
            </div>
        </div>
        
        <div>
            <SectionHeader text= "Procedurally Animated Piano" />
            <TextInsert text='
                Using a MIDI parser plugin,
                I made a <strong>Blender Geometry Node</strong> to procedurally 
                animate my piano mesh.
            '/>

            <div class='grid-container'>
                <div class="grid-item">
                    <iframe class="image" width="100%" height="300px" src="https://www.youtube.com/embed/IKBP6mFvK4c?si=pm8OBwTtK39oZb0p" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </div>
                <div class="grid-item">
                    <img class="image" src="/tsncb/PianoGeoNodes.jpg" alt="They Shall Not Come Back" />
                </div>
            </div>
        </div>
        
        

        <div>
            <SectionHeader text= "Other Gameplay"/>
        
            <div class='grid-container'>
                <div class="grid-item">
                    <img class="image"  src="/tsncb/Grabbable.webp" alt="They Shall Not Come Back" />
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