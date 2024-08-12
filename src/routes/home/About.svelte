<script>
    export let about;
</script>

<section class="about-section p-10 text-center flex flex-col items-center">

    <h2 class="text-4xl font-bold mb-5">{about.title}</h2>

    <!-- Some paragraphs -->
    <p class="text-2xl w-full md:w-4/5">
        {#each about.content as paragraph}
            {paragraph}
            <br/><br/>
        {/each}
    </p>

</section>