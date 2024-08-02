
<script>
    // Mock data for demonstration
    export let items = [
        {
            id: 1,
            date: 'February 2022',
            title: 'Application UI code in Tailwind CSS',
            description: 'Get access to over 20+ pages including a dashboard layout, charts, kanban board, calendar, and pre-order E-commerce & Marketing pages.',
        },
        {
            id: 2,
            date: 'March 2022',
            title: 'Design System Update',
            description: 'Update the design system with new components and guidelines to improve the user interface consistency across applications.',
        },
        {
            id: 3,
            date: 'April 2022',
            title: 'API Integration',
            description: 'Integrate the application with new APIs to enhance data fetching and improve functionality.',
        },
        {
            id: 4,
            date: 'May 2022',
            title: 'User Feedback Review',
            description: 'Collect and review user feedback to make necessary adjustments and improvements to the user experience.',
        },
        {
            id: 5,
            date: 'June 2022',
            title: 'Performance Optimization',
            description: 'Optimize application performance by implementing lazy loading, reducing bundle size, and improving load times.',
        },
    ];
</script>

<ol class="relative border-s m-6">
    {#each items as item (item.id)}
        <li class="mb-10 ms-4">
            <!-- circle -->
            <div class="absolute variant-filled-primary w-3 h-3 rounded-full mt-1.5 -start-1.5"></div>
            <!-- date -->
            <time class="mb-1 text-sm text-gray-400">{item.date}</time>
            <!-- title -->
            <h3 class="text-lg font-semibold text-gray-900 dark:text-white">{item.title}</h3>
            <!-- description -->
            <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">{item.description}</p>
        </li>
    {/each}
</ol>
