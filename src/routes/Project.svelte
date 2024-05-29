<script lang="ts">
    export let title = '';
    export let img = '';
    export let tags: string[] = [];
    export let blogName = '';
    let href = `/devlogs/${blogName}`;
</script>

<a href={href}>
    <div class="fixed-size-component">
        <div class="img-box">
            <img src={img} alt={title}/>
        </div>
        
        <div class="title roboto-medium-italic">
            {title}
            <div class="title-underline"></div>
        </div>
        <div class="tags roboto-regular-italic">
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
        border: 2px solid var(--white);
        margin-bottom: -2.5%;
    }   

    .fixed-size-component {
        position: relative;
        width: 100%;
        height: 25vw;
        color: var(--white);
        margin: 2% 0;
        text-transform: uppercase;
        border: 2px solid var(--white);
    }

    .title {
        position: relative;
        font-size: 2.5vw;
        background-color: var(--orange);
    }

    .tags {
        display: flex;
        gap: 2%;
    }

    .tag {
        position: relative;
        margin: 1%;
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

    .roboto-regular-italic {
        font-family: "Roboto Condensed", sans-serif;
        font-weight: 400;
        font-style: italic;
    }

    .roboto-medium-italic {
        font-family: "Roboto Condensed", sans-serif;
        font-weight: 500;
        font-style: italic;
    }
</style>