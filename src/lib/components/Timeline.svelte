
<script>
    // Mock data for demonstration
    // Mock data for demonstration
    export let items = [
        {
            "id": 1,
            "icon": "fa-solid:graduation-cap",
            "date": "June 2021",
            "title": "Finished High School",
            "description": "Graduated from high school with a focus on science and mathematics."
        },
        {
            "id": 2,
            "icon": "fa6-solid:person-swimming",
            "date": "Summer 2021",
            "title": "Lifeguard",
            "description": "Worked as a lifeguard in an indoor swimming pool, ensuring the safety of swimmers and providing assistance when needed."
        },
        {
            "id": 3,
            "icon": "fa6-solid:briefcase",
            "date": "Summer 2023",
            "title": "Worked for Zero Friction",
            "description": "Gained practical experience in software development and project management while working on various projects."
        },
        {
            "id": 4,
            "icon": "fa-solid:graduation-cap",
            "date": "June 2024",
            "title": "Bachelor's in Informatics",
            "description": "Completed a Bachelor's degree in Informatics, acquiring skills in programming, data structures, and computer systems."
        },
        {
            "id": 5,
            "icon": "fa6-solid:briefcase",
            "date": "Summer 2024",
            "title": "Worked for HPC UGent",
            "description": "Contributed to high-performance computing projects, optimizing code and managing computational tasks."
        }
    ];

</script>

<ol class="relative border-s-4 border-primary-500">
    {#each items as item (item.id)}
        <li class="mb-10 ms-6">
            <!-- Icon -->
            <span class="absolute variant-filled w-7 h-7 rounded-full -start-4 badge-icon">
                <i class="iconify text-lg" data-icon="{item.icon}"></i>
            </span>
            <!-- date -->
            <time class="text-sm text-secondary-600-300-token">{item.date}</time>
            <!-- title -->
            <h3 class="text-lg font-semibold">{item.title}</h3>
            <!-- description -->
            <p class="mb-3 text-base font-normal">{item.description}</p>
        </li>
    {/each}
</ol>
