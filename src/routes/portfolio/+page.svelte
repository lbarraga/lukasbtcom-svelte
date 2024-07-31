<div class="flex space-x-1 text-yellow-500">
    {#each Array(5) as _, index}
        {#if 3 >= index + 1}
            <!-- Full Star -->
            <i class="fa-solid fa-star"></i>
        {:else if 3 >= index + 0.5}
            <!-- Half Star -->
            <i class="fa-solid fa-star-half-alt"></i>
        {:else}
            <!-- Empty Star -->
            <i class="fa-regular fa-star"></i>
        {/if}
    {/each}
</div>