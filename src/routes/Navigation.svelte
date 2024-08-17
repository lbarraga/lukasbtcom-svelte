<script>
    import { getDrawerStore } from "@skeletonlabs/skeleton";

    const drawerStore = getDrawerStore();

    function drawerClose() {
        drawerStore.close();
    }

</script>

<nav class="list-nav p-4">
    <ul>
        <li><a href="/" on:click={drawerClose}>Home</a></li>
        <li><a href="/skills" on:click={drawerClose}>Skills</a></li>
        <li><a href="/resume" on:click={drawerClose}>Resume</a></li>
        <li><a href="/contact" on:click={drawerClose}>Contact</a></li>
    </ul>
</nav>