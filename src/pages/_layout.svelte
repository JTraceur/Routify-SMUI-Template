<script>
    // Component imports:
    import Sidebar from "../components/layout/Sidebar.svelte";
    import MobileSidebar from "../components/layout/MobileSidebar.svelte";
    import Header from "../components/layout/Header.svelte";

    import { mobileNav } from "../logic/stores";

    let mobileNavOpen = false;
    const unsubscribe = mobileNav.subscribe((value) => {
        mobileNavOpen = value;
    });
</script>

<div class="layout">
    <div class="flexCentered bgPrimary" style="grid-column: span 2">
        <Header />
    </div>

    <div>
        <!-- Desktop Sidebar: -->
        <div class="desktopOnly">
            <Sidebar />
        </div>

        <!-- Mobile Sidebar: -->
        <div class="mobileOnly">
            <MobileSidebar open={mobileNavOpen} />
        </div>
    </div>

    <div id="pageContent">
        <slot />
    </div>
</div>

<!-- routify:options preload="proximity" -->

<style>
    .layout {
        display: grid;
        grid-template-columns: minmax(180px, max-content) 1fr;
        grid-template-rows: 72px 1fr;
        height: 100%;
    }
</style>
