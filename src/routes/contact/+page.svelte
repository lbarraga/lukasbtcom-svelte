<script>
    import contact from '$lib/data/contact.json';
</script>

<div class="m-10">
    <h1 class="text-center text-3xl font-extrabold">Contact</h1>
    <p class="w-full text-center font-bold mt-4">
        If you have any questions or would like to collaborate, don't hesitate to reach out.
    </p>
</div>

<div class="logo-cloud grid-cols-1 lg:!grid-cols-2 gap-5 m-10">
    {#each contact as { href, icon, text }}
        <a class="logo-item" href={href} target="_blank">
            <i class="iconify" data-icon={icon}></i>
            <span>{text}</span>
        </a>
    {/each}
</div>

