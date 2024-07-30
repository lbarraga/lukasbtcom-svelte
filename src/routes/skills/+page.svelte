<script>
    import ExploreCard from "$lib/navigation/ExploreCard.svelte";
</script>

<div class="grid grid-cols-1 md:grid-cols-2 gap-4 m-5">
    <ExploreCard
            title="Skills"
            description="Explore the skills I've acquired over the years."
            icon="fa-tools"
            link="/skills"
    />
    <ExploreCard
            title="Resume"
            description="View my resume and learn more about my professional experience."
            icon="fa-file-alt"
            link="/resume"
    />
    <ExploreCard
            title="Portfolio"
            description="Discover the projects I've worked on and the technologies I've used."
            icon="fa-paint-brush"
            link="/portfolio"
    />
    <ExploreCard
            title="Contact"
            description="Get in touch with me and let's connect!"
            icon="fa-user-friends"
            link="/contact"
    />
</div>

