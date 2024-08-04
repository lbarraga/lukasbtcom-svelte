<script>
    import ImageOfMe from "$lib/images/me-bw.jpg"
</script>

<div class="flex flex-col md:flex-row items-center m-10">
    <img class="rounded-3xl w-4/5 md:w-1/3 h-auto" src={ImageOfMe} alt="Me" />
    <div class="flex items-center justify-center">
        <div class="md:w-4/5 text-center md:text-left mt-5">
            <p class="text-3xl md:text-6xl font-bold leading-snug">
                Hi, I'm<br/>
                <span class="font-extrabold text-tertiary-500">Lukas Barragan Torres</span>,<br/>
                a <span class="font-extrabold text-tertiary-500">Computer Science</span> student passionate about
                <span class="font-extrabold text-tertiary-500">tech</span>.
            </p>
        </div>
    </div>
</div>