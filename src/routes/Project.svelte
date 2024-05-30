<script lang="ts">
    export let title = '';
    export let role = '';
    export let background = '';
    export let logo = '';
    export let tags: string[] = [];
    export let blogName = '';
    let href = `/devlogs/${blogName}`;
    
</script>

<a href={href}>
    <div class="fixed-size-component">
        <div class="img-box">
            <img class='logo' src={logo} alt=' ' data-alt={title}/>
            <img class='background' src={background} alt=''/>
        </div>
        
        <div class="title roboto-condensed-medium-italic">
            {role}
            <div class="title-underline"></div>
        </div>
        <div class="tags roboto-condensed-regular-italic">
            {#each tags as tag}
                <span class="tag">{tag}</span>
            {/each}
        </div>
    </div>
</a>

<style>
    .img-box {
       position: relative;
        width: 95%;
        height: 75%;
        left: 5%;

        margin-bottom: -16px;
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
        /* transform: scale(1.2); */
        
    }

    .background:hover {
        transform: scale(1.1);
    }

    .fixed-size-component {
        position: relative;
        width: 100%;
        height: 500px;
        color: var(--white);
        margin: 32px 0;
        text-transform: uppercase;
    }

    .title {
        position: relative;
        font-size: 52px;
        background-color: var(--orange);
        margin-right: 6%;
        padding-left: 2%;
        transition:cubic-bezier(1, 0, 0, 1) 0.3s;
    }

    .title:hover{
        margin-right: 0;
    }

    .tags {
        display: flex;
        gap: 2%;
        font-size: 20px;
    }

    .tag {
        position: relative;
        margin: 1%;
        line-height: 1.5;
    }

    .tag:after {
        content: '';
        position: absolute;
        left: 0;
        bottom: 1px; /* Adjust underline distance */
        height: 5px; /* Adjust thickness */
        width: 100%;
        background-color: var(--orange); /* Adjust color */
    }


</style>