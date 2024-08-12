<script>
    import ExploreCard from "./ExploreCard.svelte";
    export let explore;

</script>


<h1 class="p-10 text-center text-3xl font-extrabold">
    {explore.title}
</h1>

<div class="grid grid-cols-1 md:grid-cols-2 gap-4 m-5">
    {#each explore.content as item}
        <ExploreCard {...item}/>
    {/each}
</div>
