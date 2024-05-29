<script>
    import Sidebar from './Sidebar.svelte';
</script>

<div class="page-container">
    <Sidebar/>

    <div class="content-wrap">
        <slot/>
    </div>

    <img src="/Footer.svg" alt="Footer" class="footer" />
</div>

<style>
    .page-container {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }

    .content-wrap {
        flex: 1 0 auto; /* This will make the content wrap grow if there's space available */
    }

    .footer {
        flex-shrink: 0; /* This will prevent the footer from shrinking */
        width: 100%;
        height: auto;
    }
</style>