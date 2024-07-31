<script>
    import {Ratings} from "@skeletonlabs/skeleton";

    export let value = 0;
    export let max = 5;
</script>


<Ratings {value} {max}>
    <svelte:fragment slot="empty"><i class="fa-regular fa-star"></i></svelte:fragment>
    <svelte:fragment slot="half"><i class="fa-solid fa-star-half-alt"></i></svelte:fragment>
    <svelte:fragment slot="full"><i class="fa-solid fa-star"></i></svelte:fragment>
</Ratings>