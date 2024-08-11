<script>
    import Hero from "$lib/components/Hero.svelte";
    import ExploreMyWebsite from "./ExploreMyWebsite.svelte";

    let scrollTarget;

    function scrollToElement() {
        if (scrollTarget) {
            scrollTarget.scrollIntoView({ behavior: "smooth" });
        }
    }
</script>

<Hero {scrollToElement}/>
<hr bind:this={scrollTarget}/>

<section class="about-section p-10 text-center flex flex-col items-center">
    <h2 class="text-4xl font-bold mb-5">About Me</h2>
    <p class="text-xl w-full md:w-2/3">
        👋 Hello, I'm Lukas Barragan Torres,
        a third-year Computer Science 🎓 student with a burning passion for all things tech 💻.
        Outside of my studies, I cherish the moments spent with my wonderful girlfriend,
        Charlotte Lenders ❤️. When we're not exploring the digital world together,
        I enjoy spending time swimming 🏊, mastering chess ♟️, and hitting the gym 🏋️‍♂️.
        As an avid Linux user 🐧 and an AI enthusiast 🤖, I'm captivated by the ways technology is shaping our future.
        It's a field I aspire to make my mark in 🌠.
        🛠️ In my spare time, I work on various projects that help me apply and deepen my technical skills 🌱.
        Feel free to explore more about me and let's connect! 👥
    </p>
</section>

<ExploreMyWebsite/>


<div />