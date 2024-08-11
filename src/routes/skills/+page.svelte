<!-- src/pages/SkillsPage.svelte -->
<script>
    import Skill from "./Skill.svelte";
    import { getModalStore } from '@skeletonlabs/skeleton';

    const modalStore = getModalStore();

    const modal = {
        type: 'component',
        component: 'modalComponentOne',
    };


    // Skill data for various categories
    const skills = [
        {
            skill: "Frontend Development",
            technologies: [
                { name: 'JavaScript', icon: 'fa6-brands:js' , value: 2},
                { name: 'HTML', icon: 'fa6-brands:html5', value: 1.5},
                { name: 'CSS', icon: 'fa6-brands:css3-alt', value: 1},
                { name: 'React', icon: 'fa6-brands:react', value: 1.5},
                { name: 'Svelte', icon: 'ri:svelte-line', value: 1.5},
                { name: 'Tailwind', icon: 'mdi:tailwind', value: 1.5},
            ],
            description: 'Experience with building responsive and interactive web applications using modern frontend technologies.',
            projects: [
                { title: 'Portfolio Website', icon: 'fa-solid fa-laptop', link: 'https://your-portfolio-link.com' },
                { title: 'E-commerce Site', icon: 'fa-solid fa-store', link: 'https://your-ecommerce-link.com'},
            ]
        },
        {
            skill: "Backend Development",
            technologies: [
                { name: 'Python', icon: 'fa6-brands:python', value: 3},
                { name: 'FastApi', icon: 'simple-icons:fastapi', value: 2},
                { name: 'Pydantic', icon: 'simple-icons:pydantic', value: 2},
                { name: 'SQLAlchemy', icon: 'simple-icons:sqlalchemy', value: 1.5},
            ],
            description: 'Experience with building responsive and interactive web applications using modern frontend technologies.',
            projects: [
                { title: 'Portfolio Website', icon: 'fa-solid fa-laptop', link: 'https://your-portfolio-link.com' },
                { title: 'E-commerce Site', icon: 'fa-solid fa-store', link: 'https://your-ecommerce-link.com'},
            ]
        },
        {
            skill: "Other Programming Languages",
            technologies: [
                { name: 'C', icon: 'mdi:language-c', value: 2},
                { name: 'Java', icon: 'ri:java-fill', value: 2.5},
                { name: 'C#', icon: 'tabler:brand-c-sharp', value: 2},
                { name: 'Kotlin', icon: 'mdi:language-kotlin', value: 1.5},
                { name: 'Haskell', icon: 'simple-icons:haskell', value: 1.5},
                { name: 'Prolog', icon: 'devicon-plain:prolog', value: 2},
            ],
            description: 'Proficient in various programming languages.',
            projects: [
                { title: 'Python Projects Collection', icon: 'fa-solid fa-code', link: 'https://your-python-projects-link.com'},
            ]
        },
        {
            skill: "Natural Languages",
            technologies: [
                { name: 'English', icon: 'material-symbols:language', value: 2.5},
                { name: 'Spanish', icon: 'material-symbols:language', value: 2},
                { name: 'Dutch', icon: 'material-symbols:language', value: 3},
            ],
            description: 'Fluent in multiple spoken languages.',
            projects: []
        },
        {
            skill: "Database Management",
            technologies: [
                { name: 'SQL', icon: 'tabler:sql', value: 1.5},
                { name: 'PostgreSQL', icon: 'akar-icons:postgresql-fill', value: 1.5},
                { name: 'MongoDB', icon: 'simple-icons:mongodb', value: 1.5},
            ],
            description: 'Experienced in managing and interacting with databases.',
            projects: [
                { title: 'Database Schema Design', icon: 'fa-solid fa-database', link: 'https://your-database-schema-link.com'},
            ]
        },
        {
            skill: "Version Control",
            technologies: [
                { name: 'Git', icon: 'mdi:git', value: 2.5},
                { name: 'GitHub', icon: 'fa6-brands:github', value: 2.5},
            ],
            description: 'Proficient with version control systems.',
            projects: [
                { title: 'GitHub Repositories', icon: 'fa-brands fa-github', link: 'https://your-github-repos-link.com'},
            ]
        },
        {
            skill: "Operating Systems",
            technologies: [
                { name: 'Linux', icon: 'fa6-brands:linux', value: 2},
                { name: 'Windows', icon: 'fa6-brands:windows', value: 2},
            ],
            description: 'Experienced with various operating systems.',
            projects: [
                { title: 'Linux Customization Guide', icon: 'fa-solid fa-cogs', link: 'https://your-linux-guide-link.com'},
            ]
        },
        {
            skill: "Other Tools",
            technologies: [
                { name: 'Docker', icon: 'mdi:docker', value: 2},
                { name: 'Synology NAS', icon: 'arcticons:synology-assistant', value: 1.5},
                { name: 'Bash', icon: 'devicon-plain:bash', value: 2},
                { name: 'Microsoft Azure', icon: 'devicon-plain:azure', value: 1},
            ],
            description: 'Familiar with various tools and platforms.',
            projects: [
                { title: 'Docker Container Management', icon: 'fa-brands fa-docker', link: 'https://your-docker-link.com', value: 10000},
                { title: 'Azure Deployment Scripts', icon: 'fa-brands fa-microsoft', link: 'https://your-azure-scripts-link.com' }
            ]
        }
    ];


</script>

<div class="p-6 mx-auto">
    <!-- Page Title -->
    <div class="text-center mb-6">
        <div class="flex justify-center items-center">
            <h1 class="text-3xl font-bold">Skills Overview</h1>
            <button type="button" class="btn-icon !bg-transparent" on:click={() => modalStore.trigger(modal)}>
                <i class="iconify" data-icon="material-symbols:info"></i>
            </button>
        </div>
    </div>



    <!-- Grid Layout for Skill Components -->
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 gap-6">
        {#each skills as skillData}
            <Skill
                    skill={skillData.skill}
                    technologies={skillData.technologies}
                    description={skillData.description}
                    projects={skillData.projects}
            />
        {/each}
    </div>
</div>