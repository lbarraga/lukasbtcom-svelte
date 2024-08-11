<script>
    import ProjectCard from "./ProjectCard.svelte";
    import { page } from '$app/stores'

    import data from "$lib/data/projects.json";

    let  searchString = $page.url.searchParams.get('search') || ""

    $: filteredData = data.filter(item => {
        const searchTerm = searchString.toLowerCase();
        return (
            item.title.toLowerCase().includes(searchTerm) ||
            item.description.toLowerCase().includes(searchTerm) ||
            item.bullets.some(bullet => bullet.toLowerCase().includes(searchTerm)) ||
            item.id === searchTerm
        );
    });

</script>


<div class="flex justify-center items-center w-full">
    <input class="input w-3/4 md:w-1/2 p-2 mt-10 text-lg"
           type="search"
           bind:value={searchString}
           placeholder="Search..." />
</div>

<ul>
    {#each filteredData as item}
        <li>
            <ProjectCard
                title={item.title}
                description={item.description}
                avatar={item.avatar}
                link={item.link}
                bullets={item.bullets}
            />
        </li>
    {/each}
</ul>