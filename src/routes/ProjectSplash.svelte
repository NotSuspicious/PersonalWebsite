<script>
    export let title = '';
    export let background = '';
    export let award = '';
    export let logo = '';
    import BackButton from "./BackButton.svelte";
</script>


    <div class="fixed-size-component">
        <div class="back-button">
            <BackButton/>
        </div>
        <img class='award' src={award} alt=''/>
        <div class="img-box">
            <img class='logo' src={logo} alt=' ' data-alt={title}/>
            <img class='background' src={background} alt=''/>
        </div>
    </div>
    <div class="title roboto-condensed-medium-italic">
            {title}
            <div class="title-underline"></div>
    </div>


<style>
    .fixed-size-component {
        position: relative;
        width: 100%;
        height: 300px;
        color: var(--white);
        text-transform: uppercase;
    }

    .img-box {
       position: relative;
        width: 100%;
        height: 100%;
        left: 0;
        overflow: hidden;
        
    }   

    .img-box img::after {
        content: attr(data-alt);
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        color: white;
        background-color: rgb(0, 0, 0, 0.1);
        display: flex;
        justify-content: center;
        align-items: center;
        transition: opacity 0.3s;
        pointer-events: none;

        font-family: "Roboto Condensed", sans-serif;
        font-weight: 900;
        font-style: italic;

        font-size: min(4vw, 80px);
    }

    .award {
        position: absolute;
        top: -24px;
        right: -24px;
        height: 40%;
        object-fit: cover;
        z-index: 1;
    }

    .back-button {
        position: absolute;
        top: -24px;
        left: -24px;
        z-index: 1;
    }


    .logo {
        position: absolute; /* Add this line */
        top: 50%; /* Add this line */
        left: 50%; /* Add this line */
        transform: translate(-50%, -50%); /* Add this line */
        object-fit: contain;
        height: 100%;
        width: 100%;
        
    }

    .background {
        object-fit: cover;
        height: 100%;
        width: 100%;    
    }

    .title {
        position: relative;
        font-size: 52px;
        background-color: var(--orange);
        color: white;
        height: 36px;
        margin-top: -36px;
        margin-right: 10%;
        margin-left: -24px;
        padding-left: 2%;
    }
</style>