<script>
    import { Avatar } from "@skeletonlabs/skeleton";

    export let title;
    export let description;
    export let link;
    export let avatar;
    export let bullets;
</script>

<div class="relative card variant-soft-primary p-6 m-10 card-hover flex items-start space-x-6">
    <!-- Icon -->
    <Avatar src={avatar} width="w-64" rounded="rounded-full" />

    <!-- Content -->
    <div class="flex-1">
        <h3 class="text-2xl font-bold mb-3 text-primary-800-100-token">
            {title}
        </h3>
        <p class="text-base mb-6 text-primary-800-100-token">
            {description}
        </p>

        <ul class="list-disc pl-6 space-y-4">
            {#each bullets as item}
                <li class="flex items-center space-x-2">
                    <i class="fa-solid fa-gem"></i>
                    <span class="flex-auto">{item}</span>
                </li>
            {/each}
        </ul>
    </div>

    <div class="p-10 self-center">
        <a href={link} class="font-bold hover:underline">View on Github</a>
    </div>
</div>


