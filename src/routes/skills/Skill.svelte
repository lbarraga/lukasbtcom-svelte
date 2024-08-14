<script>
    import StarRating from "./StarRating.svelte";

    export let skill;
    export let technologies;
    export let description;
    export let projects; // List of projects
</script>

<div class="p-6 variant-soft-surface m-5 space-y-4 text-center border border-gray-200 rounded-lg shadow-md flex flex-col h-full">
    <!-- Skill Title -->
    <div>
        <h1 class="text-2xl font-semibold mb-4">{skill}</h1>
    </div>

    <hr class="my-4"/>

    <!-- Technology Icons -->
    <div class="flex flex-wrap justify-around items-center mb-4">
        {#each technologies as tech}
            <div class="flex flex-col items-center text-center m-2">
                <i class="iconify text-5xl" data-icon="{tech.icon}"></i>
                <span class="mt-2 text-lg font-medium">{tech.name}</span>
                <StarRating className="text-xs mt-1" value={tech.stars} max={3}/>
            </div>
        {/each}
    </div>

    <hr class="my-4"/>

    <!-- Description -->
    <div class="mb-4 flex-grow">
        <p>{description}</p>
    </div>

    <!-- Projects List -->
    <ul class="space-y-4">
        {#each projects as project}
            <li>
                <a href={project.link} class="card-hover variant-soft-surface flex items-center p-4">
                    <!-- Icon -->
                    <!--i class="iconify text-3xl" data-icon={project.icon}></i-->

                    <!-- Title -->
                    <h3 class="flex-auto text-lg font-semibold">
                        {project.title}
                    </h3>

                    <!-- Arrow Icon -->
                    <span>
                        <i class="fa-solid fa-arrow-right text-xl"></i>
                    </span>
                </a>
            </li>
        {/each}
    </ul>
</div>
