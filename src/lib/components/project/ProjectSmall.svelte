<script>
    import projects from "$lib/data/projects.json";

    export let project;

    let projectData = projects.find(p => p.id === project);
</script>

<li>
    <a href="/portfolio?search={projectData.id}">

        <!-- Icon -->
        <span class="badge-icon bg-primary-500">
            <i class="{projectData.icon} fa-2x"></i>
        </span>

        <!-- Title -->
        <h3 class="flex-auto">
            {projectData.title}
        </h3>

        <!-- Arrow Icon -->
        <span>
            <i class="fa-solid fa-arrow-right text-xl"></i>
        </span>
    </a>
</li>