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
            title="Computational Fluid Dynamics"
            logo="/cfd/logo-large.png"
            background="/cfd/background.png"
        />
        <div/>
        <div class='grid-container'>
            <div class="grid-item">
                <TextInsert text="
                    During Winter 2023, I tried to implement fluid mechanics for a game idea that I had. Little did I know how complicated and fascinating it would be. I fell down a rabbit hole of computational fluid dynamics; and I'm still falling!
                    <br><br>Here are some of the things I've made so far!
                "/>
            </div>
        </div>
        <div>
            <SectionHeader text= "Euler Equation Solver" />
            <div class='grid-container'>
                <div class="grid-item">
                    <TextInsert text="
                        Over the summer of 2024, I attended a computational fluid dynamics workshop hosted by <strong>USC Center of Advanced Research Computing</strong>.
                        <br>
                    <br> - Developed an <strong>Euler Equation solver</strong> on a structured grid using Numpy, optimized for parallel computing on USC’s supercomputer.
                    <br> - Accelerated simulation speed by 300% through parallel GPU computing with <strong>CUDA Python</strong>.
                    "/>
                </div>
                <div class="grid-item">
                    <iframe class="image" width="100%" height="300px" src="https://www.youtube.com/embed/lWHH4D7yxAY?si=bb73GsdRguRkfLsy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </div>
            </div>
        </div>
        
        <div>
            <SectionHeader text= "Smoothed Particle Hydrodynamics" />
            <div class='grid-container'>
                <div class="grid-item">
                    <TextInsert text="
                        Engineered a real-time smoothed particle hydrodynamics simulation with raymarched rendering techniques and real-time collision.
                        <br>
                        <br> - Wrote a SPH <strong>compute shader</strong> in <strong>HLSL</strong> and implemented it in Unity's <strong>URP</strong>.
                        <br> - My simulation doesn't have a very efficient ray marching implementation, and there is a lot of turbulence, but I'm planning on optimizing my simulation!
                    "/>
                </div>
                <div class="grid-item">
                    <iframe class="image" width="100%" height="300px" src="https://www.youtube.com/embed/vcY7p4MAJUQ?si=GnTmpi5t0HurJAVR" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </div>
            </div>
        </div>

        <div>
            <SectionHeader text= "Houdini FLIP Solver" />
            <div class='grid-container'>
                <div class="grid-item">
                    <TextInsert text="
                        To gain experience with <strong>Houdini</strong> and their <strong>FLIP Solver</strong>, I made this small render!
                        <br>
                        <br> - Learned how to use Houdini's <strong>FLIP Fluids</strong> to simulate fluid dynamics.
                        <br> - Used Solaris to render fluids and glass.
                        <br> - Used <strong>Logic Pro</strong> to design the sound effects.
                    "/>
                </div>
                <div class="grid-item">
                    <iframe class="image" width="100%" height="300px" src="https://www.youtube.com/embed/iFu9cCE0MmU?si=ecAcS27FO2p_mEkt" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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