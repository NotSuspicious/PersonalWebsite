<script lang="ts">
    export let title = '';
    export let role = '';
    export let background = '';
    export let award = '';
    export let logo = '';
    export let blogName = '';
    let href = `/devlogs/${blogName}`;

    let isHovered = false;
    
</script>

    <div class="fixed-size-component">
        <img class='award' src={award} alt=''/>
        <a href={href}>
            <!-- svelte-ignore a11y-no-static-element-interactions -->
            <div class="img-box" 
                on:mouseenter={() => isHovered = true} 
                on:mouseleave={() => isHovered = false}
            >
                <img class='logo' src={logo} alt=' ' data-alt={title}
                    class:img-hovered={isHovered}/>
                <img class='background' src={background} alt=''
                    class:img-hovered={isHovered}/>
            </div>
        </a>
        
        
        <div class="title roboto-condensed-medium-italic"
            class:img-hovered={isHovered}>
            {role}
            <div class="title-underline"></div>
        </div>
        <!-- <div class="tags roboto-condensed-regular-italic">
            {#each tags as tag}
                <span class="tag">{tag}</span>
            {/each}
        </div> -->
    </div>

<style>
    .fixed-size-component {
        position: relative;
        width: 100%;
        height: 360px;
        color: var(--white);
        margin-bottom: 100px;
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

    .logo {
        position: absolute; /* Add this line */
        top: 50%; /* Add this line */
        left: 50%; /* Add this line */
        transform: translate(-50%, -50%); /* Add this line */
        object-fit: contain;
        height: 100%;
        width: 100%;
        
    }

    .img-hovered.background {
        transform: scale(1.05);
    }

    .img-hovered.logo {
        z-index: 2;
    }

    .img-hovered.title {
        margin-right: 24px;
    }

    .logo {
        z-index: 2;
    }

    .award {
        position: absolute;
        top: -18px;
        right: -3%;
        height: 25%;
        object-fit: cover;
        z-index: 1;
    }


    .background {
        object-fit: cover;
        height: 100%;
        width: 100%;
        transition:ease-in-out 0.15s;
        
    }

    .title {
        position: relative;
        font-size: 52px;
        background-color: var(--orange);
        height: 36px;
        margin-top: -18px;
        margin-bottom: 18px;
        margin-right: 24px;
        margin-left: -14px;
        padding-left: 24px;
        transition:cubic-bezier(1, 0, 0, 1) 0.15s;
    }

</style>
