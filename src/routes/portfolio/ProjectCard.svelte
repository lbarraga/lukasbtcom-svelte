<script>
    import { Avatar } from "@skeletonlabs/skeleton";

    export let title;
    export let description;
    export let link;
    export let avatar;
    export let bullets;
</script>

<div class="relative card variant-soft-surface p-6 m-10 card-hover flex flex-col items-center lg:flex-row lg:items-start space-y-6 lg:space-y-0 lg:space-x-6">
    <!-- Icon -->
    <div class="flex-shrink-0 lg:mr-6">
        <Avatar src={avatar} width="w-32 lg:w-64" rounded="rounded-full" />
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
        <ul class="list-disc pl-6 space-y-4 text-left lg:text-left">
            {#each bullets as item}
                <li class="flex items-center space-x-2">
                    <i class="fa-solid fa-gem"></i>
                    <span class="flex-auto text-sm lg:text-base">{item}</span>
                </li>
            {/each}
        </ul>
    </div>

    <div class="p-10 self-center">
        <a href={link} class="font-bold hover:underline">View on Github</a>
    </div>
</div>
