<script>
    import { Accordion } from "@skeletonlabs/skeleton";
    import Skill from "$lib/components/Skill.svelte";

    let skills = [
        {
            icon: "fa-brands fa-python",
            summary: "Skilled in Python for a range of applications, from data manipulation and web scraping to automation and AI.",
            value: 4.5,
            projects: ["reddit-video-storyteller"]
        },
        {
            icon: "fa-brands fa-js",
            summary: "Experienced in JavaScript for dynamic web development, including both frontend and backend frameworks.",
            value: 4,
            projects: ["personal-website"]
        },
        {
            icon: "fa-brands fa-java",
            summary: "Proficient in Java for building robust and scalable applications, with knowledge of various Java frameworks.",
            value: 4,
            projects: ["two-three-tree-java"]
        },
        {
            icon: "fa-brands fa-css3-alt",
            summary: "Skilled in CSS for styling web pages, with experience in modern CSS techniques and frameworks.",
            value: 3,
            projects: ["personal-website"]
        },
        {
            icon: "fa-brands fa-html5",
            summary: "Experienced in HTML for structuring web content, with a focus on semantic markup and accessibility.",
            value: 3,
            projects: ["personal-website"]
        }
    ];

</script>

<div class="p-8">
    <Accordion class="space-y-5">
        {#each skills as skill}
            <Skill {...skill}/>
        {/each}
    </Accordion>
</div>