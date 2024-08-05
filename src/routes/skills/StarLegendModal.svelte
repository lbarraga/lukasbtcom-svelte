<script>
    import { getModalStore } from '@skeletonlabs/skeleton';
    import StarRating from "$lib/components/StarRating.svelte";

    const modalStore = getModalStore();

    // Base Classes
    const cBase = 'card p-4 w-modal shadow-xl space-y-4';
    const cHeader = 'text-2xl font-bold';

    // Star rating legend data
    const starLegend = [
        { value: 1, text: "I can find my way with some effort and a search engine" },
        { value: 2, text: "I know general concepts and/or can apply knowledge from other fields" },
        { value: 3, text: "I am very confident in my skills" }
    ];
</script>

{#if $modalStore[0]}
    <div class="modal-example-form {cBase}">
        <header class={cHeader}>Star Legend</header>
        <article class="space-y-2">
            {#each starLegend as legend}
                <div class="flex items-center space-x-4">
                    <div class="w-16 flex justify-center">
                        <StarRating class="text-xs" value={legend.value} max={3} />
                    </div>
                    <span class="flex-1 text-left break-words">{legend.text}</span>
                </div>
            {/each}
        </article>
    </div>
{/if}
