<script>
    import { Accordion } from "@skeletonlabs/skeleton";
    import Skill from "$lib/components/Skill.svelte";

    let skills = [
        {
            icon: "fa-brands fa-python",
            summary: "Skilled in Python for a range of applications, from data manipulation and web scraping to automation and AI.",
            value: 4.5,
            projects: [
                {
                    title: "VideoStoryteller: Bringing Stories to Life!",
                    icon: "fa-solid fa-book",
                    href: "/project/1"
                },
                {
                    title: "DataAnalyzer: Insightful Data Analysis",
                    icon: "fa-solid fa-chart-line",
                    href: "/project/2"
                }
            ]
        },
        {
            icon: "fa-brands fa-js",
            summary: "Experienced in JavaScript for dynamic web development, including both frontend and backend frameworks.",
            value: 4,
            projects: [
                {
                    title: "WebInteractive: Dynamic Web Experiences",
                    icon: "fa-solid fa-laptop-code",
                    href: "/project/3"
                },
                {
                    title: "BackendMaster: Efficient Server Solutions",
                    icon: "fa-solid fa-server",
                    href: "/project/4"
                }
            ]
        },
        {
            icon: "fa-brands fa-java",
            summary: "Proficient in Java for building robust and scalable applications, with knowledge of various Java frameworks.",
            value: 4,
            projects: [
                {
                    title: "EnterpriseApp: Scalable Business Solutions",
                    icon: "fa-solid fa-building",
                    href: "/project/5"
                },
                {
                    title: "JavaSpring: Advanced Spring Applications",
                    icon: "fa-solid fa-leaf",
                    href: "/project/6"
                }
            ]
        },
        {
            icon: "fa-brands fa-css3-alt",
            summary: "Skilled in CSS for styling web pages, with experience in modern CSS techniques and frameworks.",
            value: 3,
            projects: [
                {
                    title: "StylingWizard: Modern CSS Techniques",
                    icon: "fa-solid fa-palette",
                    href: "/project/7"
                },
                {
                    title: "ResponsiveDesign: Mobile-First Approach",
                    icon: "fa-solid fa-mobile-alt",
                    href: "/project/8"
                }
            ]
        },
        {
            icon: "fa-brands fa-html5",
            summary: "Experienced in HTML for structuring web content, with a focus on semantic markup and accessibility.",
            value: 3,
            projects: [
                {
                    title: "WebStructure: Semantic HTML Mastery",
                    icon: "fa-solid fa-code",
                    href: "/project/9"
                },
                {
                    title: "AccessibleWeb: Inclusive Web Design",
                    icon: "fa-solid fa-universal-access",
                    href: "/project/10"
                }
            ]
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