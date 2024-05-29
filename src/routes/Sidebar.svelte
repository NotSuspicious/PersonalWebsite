<script>
    import SidebarElement from './SidebarElement.svelte';
</script>

<div class="sidebar">
    <SidebarElement title="Home" href="/"/>
    <SidebarElement title="Fun" href="/fun"/>
    <SidebarElement title="Music" href="music"/>
</div>

<style>
    .sidebar {
        width: 108px;
        height: 80vh;
        position: fixed;
        right: 0;
        top: 0;
    }
</style>