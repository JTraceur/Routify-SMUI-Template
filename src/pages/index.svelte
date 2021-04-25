<script>
    // Routify import:
    import { metatags } from '@roxi/routify';
    metatags.title = 'Student Central';
    metatags.description = 'Management for EST Classes';

    // Component imports:
    import Sidebar from '../components/layout/Sidebar.svelte'
    import MobileSidebar from '../components/layout/MobileSidebar.svelte'
    import Header from '../components/layout/Header.svelte'

    import { mobileNav } from '../logic/stores';

    let mobileNavOpen = false;
    const unsubscribe = mobileNav.subscribe(value => { 
        mobileNavOpen = value; 
    });
</script>

<div class="layout">
    <div class="flexCentered bgPrimary" style="grid-column: span 2">
        <Header></Header>
    </div>

    <div>
        <!-- Desktop Sidebar: -->
        <div class="desktopOnly">
            <Sidebar></Sidebar>
        </div>
        
        <!-- Mobile Sidebar: -->
        <div class="mobileOnly">
            <MobileSidebar open={mobileNavOpen}></MobileSidebar>
        </div>
    </div>
</div>

<style>
    .layout {
        display: grid;
        grid-template-columns: minmax(180px, max-content) 1fr;
        grid-template-rows: 72px 1fr;
        height: 100%;
    }
</style>