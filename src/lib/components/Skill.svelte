<script>
    import { AccordionItem } from "@skeletonlabs/skeleton";
    import StarRating from "$lib/components/StarRating.svelte";

    export let icon;
    export let summary;
    export let value;

</script>

<AccordionItem class="card-hover variant-ghost-primary">
    <svelte:fragment slot="lead">
        <i class="{icon} fa-5x"></i>
    </svelte:fragment>

    <svelte:fragment slot="summary">
        <div class="flex flex-col items-start md:items-center md:flex-row md:justify-between">
            <h1 class="font-bold mb-4 md:mb-0">
                {summary}
            </h1>

            <div class="flex items-center md:ml-4">
                <StarRating {value} max={5}/>
            </div>
        </div>
    </svelte:fragment>


    <svelte:fragment slot="content">
        <slot />
    </svelte:fragment>

</AccordionItem>