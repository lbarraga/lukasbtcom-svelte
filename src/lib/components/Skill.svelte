<script>
    import { AccordionItem } from "@skeletonlabs/skeleton";
    import StarRating from "$lib/components/StarRating.svelte";

    export let icon;
    export let summary;
    export let value;

</script>

<AccordionItem class="variant-ghost-primary">

    <svelte:fragment slot="lead">
        <i class="{icon} fa-5x"></i>
    </svelte:fragment>

    <svelte:fragment slot="summary">
        <div class="flex justify-between items-center">
            <p class="p-1 font-bold">
                {summary}
            </p>

            <div class="flex items-center pr-8">
                <StarRating {value} max={5}/>
            </div>
        </div>
    </svelte:fragment>


    <svelte:fragment slot="content">
        <slot />
    </svelte:fragment>

</AccordionItem>