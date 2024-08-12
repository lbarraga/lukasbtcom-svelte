<script>
    import { getModalStore } from '@skeletonlabs/skeleton';
    import StarRating from "./StarRating.svelte";

    import skills from '$lib/data/skills.json';

    const modalStore = getModalStore();
</script>

{#if $modalStore[0]}
    <div class="modal-example-form card p-4 w-modal shadow-xl space-y-4">
        <header class="text-2xl font-bold">
            {skills.starLegend.title}
        </header>

        <article class="space-y-2">
            {#each skills.starLegend.content as legend}
                <div class="flex items-center space-x-4">
                    <div class="w-16 flex justify-center">
                        <StarRating class="text-xs" value={legend.stars} max={3} />
                    </div>
                    <span class="flex-1 text-left break-words">{legend.text}</span>
                </div>
            {/each}
        </article>
    </div>
{/if}
