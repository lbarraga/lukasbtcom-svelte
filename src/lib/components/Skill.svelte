<script>
    import { AccordionItem } from "@skeletonlabs/skeleton";
    import StarRating from "$lib/components/StarRating.svelte";
    import ProjectSmall from "$lib/components/project/ProjectSmall.svelte";

    export let icon;
    export let summary;
    export let value;
    export let projects;

</script>

<AccordionItem class="card-hover variant-ghost-tertiary">
    <svelte:fragment slot="lead">
        <i class="{icon} fa-5x"></i>
    </svelte:fragment>

    <svelte:fragment slot="summary">
        <div class="flex flex-col items-start md:items-center md:flex-row md:justify-between">
            <h1 class="font-bold mb-4 md:mb-0">
                {summary}
            </h1>

            <div class="flex items-center md:ml-4">
                <StarRating {value} max={5}/>
            </div>
        </div>
    </svelte:fragment>


    <svelte:fragment slot="content">
        <h2 class="text-2xl font-bold mb-4">
            Projects
        </h2>
        <nav class="list-nav">
            <ul>
                {#each projects as project}
                    <ProjectSmall {project}/>
                {/each}
            </ul>
        </nav>
    </svelte:fragment>

</AccordionItem>