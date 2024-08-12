<script>
    import resume from '$lib/data/resume.json';
</script>

<ol class="relative border-s-4 border-primary-900-50-token">
    {#each resume.timeline.content as item (item.id)}
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
