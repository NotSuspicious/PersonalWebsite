<div class="text-box roboto-regular">
    <p>I’m William, a <strong>Game Developer</strong>, <strong>TECHNICAL ARTIST</strong>, and a <strong>MUSICIAN</strong>. I’m studying computer science @ USC Games.
        <br/>
        <br/>
        My greatest passion is leveraging my technical and creative skills to create multimedia experiences.
        <br/>
        <br/>
        Whether that be through <strong>PC GAMES</strong>, <strong>VR EXPERIENCES</strong>, or <strong>PHYSICS SIMULATIONS</strong>, you can always catch me working on something I love!
    </p>
</div>

<style> 
    strong {
        color: var(--highlight);
        text-transform: uppercase;
        font-style: italic;
        letter-spacing: 0px;
        font-family: "Roboto", sans-serif;
    }

    .text-box {
        display: flex;
        position: relative;
        margin: 0 0;
        color: var(--white);
        font-size: 15pt;
    }

    .text-box::before {
        content: '';
        display: block;
        width: 12px; /* Adjust width */
        height: calc(100%); /* Adjust height */
        background-color: var(--orange); /* Adjust color */
        position: absolute; /* This will make the ::before pseudo-element positioned relative to the text-box div */
        left: -36px; /* This will position the rectangle to the left of the text-box div */
        top: 0; /* This will offset the rectangle from the top of the text-box div */
    }
</style>