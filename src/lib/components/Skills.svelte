<script>
    import { Accordion } from "@skeletonlabs/skeleton";
    import Skill from "$lib/components/Skill.svelte";
    import ProjectSmall from "$lib/components/project/ProjectSmall.svelte";

    let skills = [
        {
            icon: "fa-brands fa-python",
            summary: "Skilled in Python for a range of applications, from data manipulation and web scraping to automation and AI.",
            value: 4.5
        },
        {
            icon: "fa-brands fa-js",
            summary: "Experienced in JavaScript for dynamic web development, including both frontend and backend frameworks.",
            value: 4
        },
        {
            icon: "fa-brands fa-java",
            summary: "Proficient in Java for building robust and scalable applications, with knowledge of various Java frameworks.",
            value: 4
        },
        {
            icon: "fa-brands fa-css3-alt",
            summary: "Skilled in CSS for styling web pages, with experience in modern CSS techniques and frameworks.",
            value: 3
        },
        {
            icon: "fa-brands fa-html5",
            summary: "Experienced in HTML for structuring web content, with a focus on semantic markup and accessibility.",
            value: 3
        }
    ];
</script>

<div class="p-8">
    <Accordion class="space-y-5">
        <Skill {...skills[0]}>
            <h2 class="text-2xl font-bold mb-4">
                Projects
            </h2>
            <nav class="list-nav">
                <ul>
                    <ProjectSmall
                            href="/project/1"
                            icon="fa-solid fa-book"
                            title="VideoStoryteller: Bringing Stories to Life!"
                    />
                    <ProjectSmall
                            href="/project/1"
                            icon="fa-solid fa-book"
                            title="VideoStoryteller: Bringing Stories to Life!"
                    />
                </ul>
            </nav>
        </Skill>
        <Skill {...skills[1]}/>
        <Skill {...skills[2]}/>
        <Skill {...skills[3]}/>
        <Skill {...skills[4]}/>
    </Accordion>
</div>