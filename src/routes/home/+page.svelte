<script>
    import Hero from "./Hero.svelte";
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
    <p class="text-2xl w-full md:w-4/5">
        I'm Lukas Barragan Torres,
        a first year Computer Science master student with a passion for all things tech.
        I enjoy modelling problems and creating solutions in a simple and elegant way.
        My passion for tech started at 14 when I built a side scrolling adventure game with scratch.
        Later on, I learned to code in Python and Java.
        <br/><br/>
        My studies have provided me with a broad understanding of various facets of computer science.
        While I may not specialize deeply in one area, this diverse knowledge allows me to see the bigger picture,
        make connections between different concepts, and approach problems from multiple angles.
        <br/><br/>
        When I'm not behind a screen,
        I enjoy spending time swimming, mastering chess, going to the gym and spending time with my girlfriend Charlotte.
        As an avid Linux user and an open-source enthusiast,
        I'm captivated by the ways free technology is shaping our future.
        In my spare time, I work on various projects that help me apply and deepen my technical skills.
        Feel free to explore more about me and let's connect!
    </p>
</section>

<ExploreMyWebsite/>


<div />