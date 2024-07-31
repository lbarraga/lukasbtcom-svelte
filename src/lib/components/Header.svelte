<script>
    import {AppBar, getDrawerStore, LightSwitch} from "@skeletonlabs/skeleton";

    const drawerStore = getDrawerStore();

    function drawerOpen() {
        drawerStore.open({});
    }
</script>

<AppBar>
    <svelte:fragment slot="lead">
        <div class="flex items-center">
            <button class="md:hidden btn btn-sm mr-4" on:click={drawerOpen}>
                <span>
                    <svg viewBox="0 0 100 80" class="fill-token w-4 h-4">
                        <rect width="100" height="20" />
                        <rect y="30" width="100" height="20" />
                        <rect y="60" width="100" height="20" />
                    </svg>
                </span>
            </button>
            <a href="/">
                <strong class="text-base uppercase">Lukas Barragan Torres</strong>
            </a>
        </div>
    </svelte:fragment>
    <svelte:fragment slot="trail">
        <div class="hidden md:flex space-x-4">
            <a class="btn hover:variant-soft-primary" href="/skills">Skills</a>
            <a class="btn hover:variant-soft-primary" href="/resume">Resume</a>
            <a class="btn hover:variant-soft-primary" href="/portfolio">Portfolio</a>
            <a class="btn hover:variant-soft-primary" href="/contact">Contact</a>
        </div>
        <LightSwitch />
    </svelte:fragment>
</AppBar>