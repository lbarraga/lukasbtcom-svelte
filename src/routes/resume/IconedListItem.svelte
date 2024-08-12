<script>
    export let icon;
    export let title;
    export let content;
</script>

<li class="list-none">
    <div class="flex items-start">
        <i class="iconify text-sm mr-2 flex-shrink-0 mt-1.5" data-icon="{icon}"></i>
        <div>
            <h3 class="text-lg font-bold">{title}</h3>
            <p class="mt-1">
                {content}
            </p>
        </div>
    </div>
</li>
