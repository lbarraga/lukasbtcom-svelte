<!-- src/pages/SkillsPage.svelte -->
<script>
    import Skill from "./Skill.svelte";
    import { getModalStore } from '@skeletonlabs/skeleton';

    import skills from '$lib/data/skills.json';

    const modalStore = getModalStore();

    const modal = {
        type: 'component',
        component: 'modalComponentOne',
    };


</script>

<div class="p-6 mx-auto">
    <!-- Page Title -->
    <div class="text-center mb-6">
        <div class="flex justify-center items-center">
            <h1 class="text-3xl font-bold">Skills Overview</h1>

            <!-- info icon for modal -->
            <button type="button" class="btn-icon text-xl mt-0.5" on:click={() => modalStore.trigger(modal)}>
                <i class="iconify" data-icon="material-symbols:info"></i>
            </button>
        </div>
    </div>



    <!-- Grid Layout for Skill Components -->
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 gap-6">
        {#each skills as skillData}
            <Skill {...skillData}/>
        {/each}
    </div>
</div>