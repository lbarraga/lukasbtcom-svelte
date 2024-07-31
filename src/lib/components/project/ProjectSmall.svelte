<script>
    export let href;
    export let icon;
    export let title;
</script>

<li>
    <a {href}>

        <!-- Icon -->
        <span class="badge-icon bg-primary-500">
            <i class="{icon} fa-2x"></i>
        </span>

        <!-- Title -->
        <h3 class="flex-auto">
            {title}
        </h3>
    </a>
</li>