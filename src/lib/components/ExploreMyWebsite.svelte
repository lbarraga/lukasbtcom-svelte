<script>
    import ExploreCard from "$lib/components/ExploreCard.svelte";
</script>

<h1 class="p-10 text-center text-3xl font-extrabold">
    Explore My Website
</h1>

<div class="grid grid-cols-1 md:grid-cols-2 gap-4 m-5">
    <ExploreCard
            title="Skills"
            description="Explore the skills I've acquired over the years."
            icon="fa-solid:tools"
            link="/skills"
    />
    <ExploreCard
            title="Resume"
            description="View my resume and learn more about my professional experience."
            icon="fa-solid:file-alt"
            link="/resume"
    />
    <ExploreCard
            title="Portfolio"
            description="Discover the projects I've worked on and the technologies I've used."
            icon="fa6-solid:paintbrush"
            link="/portfolio"
    />
    <ExploreCard
            title="Contact"
            description="Get in touch with me and let's connect!"
            icon="fa-solid:user-friends"
            link="/contact"
    />
</div>

