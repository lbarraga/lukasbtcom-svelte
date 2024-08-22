<script>
    import AccentText from "./AccentText.svelte";

    export let scrollToElement
</script>

<div class="flex flex-col md:flex-row items-center m-10">

    <!-- Image of me -->
    <div class="w-4/5 md:w-5/12 rounded-3xl overflow-hidden">
        <enhanced:img src="$lib/images/me-bw.jpg" alt="Me" class="w-full h-auto" />
    </div>


    <div class="flex items-center justify-center">
        <div class="md:w-4/5 text-center md:text-left mt-5">

            <p class="text-3xl md:text-6xl font-bold leading-snug">
                Hi, I'm<br/>
                <AccentText>Lukas Barragan Torres</AccentText>,<br/>
                a <AccentText>Computer Science</AccentText> student passionate about <AccentText>tech</AccentText>.
            </p>


            <button type="button" on:click={scrollToElement} class="btn-icon btn-icon-xl variant-filled mt-10">
                <i class="iconify text-5xl animate-pulse" data-icon="mdi:arrow-down" data-inline="false"></i>
            </button>
        </div>
    </div>
</div>