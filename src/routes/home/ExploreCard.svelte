<script>
    export let title;
    export let description;
    export let icon;
    export let link = '/';
</script>

<a href="{link}" class="relative card variant-soft-surface card-hover p-4 flex items-center space-x-4">
    <!-- Icon -->
    <span class="flex items-center justify-center">
        <i class="iconify text-4xl" data-icon="{icon}"></i>
    </span>

    <!-- Content -->
    <div class="flex-1">
        <h3 class="text-xl font-semibold mb-1">{title}</h3>
        <p>{description}</p>
    </div>

    <!-- Arrow Icon -->
    <span class="absolute bottom-2 right-5">
        <i class="fa-solid fa-arrow-right text-xl"></i>
    </span>
</a>
