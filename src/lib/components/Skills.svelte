<script>
    import { Accordion, AccordionItem } from "@skeletonlabs/skeleton";
</script>

<div class="p-4">
    <Accordion class="mr-10">
        <AccordionItem class="variant-ghost-primary mb-5">
            <svelte:fragment slot="lead">
                <i class="fa-brands fa-python fa-5x"></i>
            </svelte:fragment>
            <svelte:fragment slot="summary">
                <p class="p-1 font-bold">
                    Skilled in Python for a range of applications,
                    from data manipulation and web scraping to automation and AI.
                </p>
            </svelte:fragment>
        </AccordionItem>
        <AccordionItem class=" variant-ghost-primary">
            <svelte:fragment slot="lead">(icon)</svelte:fragment>
            <svelte:fragment slot="summary">(summary)</svelte:fragment>
            <svelte:fragment slot="content">(content)</svelte:fragment>
        </AccordionItem>
    </Accordion>
</div>