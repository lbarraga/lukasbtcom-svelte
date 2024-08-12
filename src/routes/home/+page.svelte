<script>
    import Hero from "./Hero.svelte";
    import ExploreMyWebsite from "./ExploreMyWebsite.svelte";
    import home from '$lib/data/home.json';
    import About from "./About.svelte";

    let scrollTarget; // <hr/> is scroll target

    function scrollToElement() {
        if (scrollTarget) {
            scrollTarget.scrollIntoView({ behavior: "smooth" });
        }
    }
</script>

<Hero {scrollToElement}/>

<hr bind:this={scrollTarget}/>

<About about={home.about}/>

<ExploreMyWebsite explore={home.explore}/>