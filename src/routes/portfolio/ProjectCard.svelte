<script>
    export let title;
    export let description;
    export let link;
    export let icon;
    export let bullets;
</script>

<div class="relative card variant-soft-surface p-6 m-10 card-hover flex flex-col items-center lg:flex-row lg:items-start space-y-6 lg:space-y-0 lg:space-x-6">
    <!-- Icon -->
    <div class="flex-shrink-0 lg:mr-6 self-center">
        <i class="iconify text-[12rem]" data-icon="{icon}"></i>
    </div>

    <div class="flex-1 text-center lg:text-left">

        <!-- Title -->
        <h3 class="text-xl lg:text-2xl font-bold mb-3 text-primary-800-100-token">
            {title}
        </h3>

        <!-- Description -->
        <p class="text-sm lg:text-base mb-6 text-primary-800-100-token">
            {description}
        </p>

        <!-- Bullets -->
        <div class="grid grid-cols-1 md:grid-cols-1 gap-4 text-left">
            {#each bullets as item}
                <div class="flex items-center space-x-2">
                    <i class="fa-solid fa-gem"></i>
                    <span class="text-sm lg:text-base">{item}</span>
                </div>
            {/each}
        </div>
    </div>

    <div class="p-10 self-center">
        <a href={link} class="font-bold hover:underline">View on Github</a>
    </div>
</div>
