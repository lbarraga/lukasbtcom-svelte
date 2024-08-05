<script>
    import Timeline from "$lib/components/Timeline.svelte";
    import profilePic from "$lib/images/me-casual.jpg";
    import { Avatar } from "@skeletonlabs/skeleton";

    // Profile and Contact Information
    const profile = {
        name: "Lukas Barragan Torres",
        title: "Student Master of Science in Computer Science",
        email: "lukas.barragantorres@UGent.be",
        linkedin: "https://linkedin.com/in/lukas-barragan-torres",
        github: "https://github.com/lbarraga",
        location: "Ghent, Belgium",
        locationLink: "https://www.google.com/maps/search/?api=1&query=Ghent,+Belgium"
    };

    // Skills data
    const skills = [
        {
            category: "Programming Languages",
            items: ["Python", "C", "Java", "C#", "JavaScript", "Kotlin", "Haskell", "Prolog"]
        },
        {
            category: "Natural Languages",
            items: ["English", "Spanish", "Dutch"]
        },
        {
            category: "Web Development",
            items: ["HTML", "CSS", "Tailwind CSS", "Svelte", "React", "FastAPI", "Pydantic"]
        },
        {
            category: "Database Management",
            items: ["SQL", "PostgreSQL", "MongoDB"]
        },
        {
            category: "Version Control",
            items: ["Git", "GitHub"]
        },
        {
            category: "Operating Systems",
            items: ["Linux", "Windows"]
        },
        {
            category: "Other Tools",
            items: ["Docker", "Bash", "Microsoft Azure"]
        }
    ];

    // Personal Statement
    const personalStatement = "I am a highly motivated and detail-oriented student pursuing a Master of Science in Computer Science. With a solid foundation in programming and a passion for technology, I aim to leverage my skills in software development and problem-solving to contribute to innovative projects and make a positive impact in the tech industry.";

    // Certifications
    const certifications = [
        {
            title: "Bachelor's in Informatics",
            institution: "University Name",
            description: "Comprehensive undergraduate program focusing on various aspects of computer science and information technology."
        },
        {
            title: "Lifeguard Certification",
            institution: "Certification Body",
            description: "Certified lifeguard with training in water safety, rescue techniques, and first aid."
        }
    ];

    // Extracurricular Activities
    const extracurricularActivities = [
        {
            title: "Swimming Instructor",
            description: "Instructed swimming lessons for various age groups and skill levels, focusing on water safety and technique improvement (6 Years)."
        },
        {
            title: "Self-Hosting Enthusiast",
            description: "Maintained a personal Synology NAS and self-hosted various applications, including web servers and databases."
        },
        {
            title: "Active in Sports and Hobbies",
            description: "Passionate about swimming, chess, and going to the gym. Regularly engage in these activities to maintain a balanced lifestyle."
        }
    ];

    // Icon data
    const icons = [
        {
            class: "fa-solid fa-envelope",
            link: `mailto:${profile.email}`,
            text: profile.email
        },
        {
            class: "fa-brands fa-linkedin",
            link: profile.linkedin,
            text: "LinkedIn"
        },
        {
            class: "fa-solid fa-map-marker-alt",
            link: profile.locationLink,
            text: profile.location
        },
        {
            class: "fa-brands fa-github",
            link: profile.github,
            text: "GitHub"
        }
    ];
</script>

<div class="variant-ghost-surface w-full md:w-3/5 mx-auto p-4 md:p-10">

    <!-- Profile Picture and Heading -->
    <div class="flex flex-col md:flex-row mb-10">
        <Avatar src={profilePic} rounded="rounded-xl" class="mb-4 md:mb-0 md:mr-4 w-44"/>
        <div>
            <h1 class="text-3xl md:text-5xl mb-2 font-extrabold">{profile.name}</h1>
            <p class="text-xl md:text-2xl">{profile.title}</p>

            <div class="flex flex-col mt-4">
                {#each icons as icon}
                    <div class="flex items-center mb-2">
                        <i class={icon.class + " text-lg md:text-xl mr-2"}></i>
                        <a href={icon.link} class="text-sm md:text-lg" target={icon.link ? "_blank" : ""}>{icon.text}</a>
                    </div>
                {/each}
            </div>
        </div>
    </div>

    <!-- Personal Statement -->
    <div class="mb-10">
        <h2 class="text-2xl md:text-4xl mb-4 font-bold">Personal Statement</h2>
        <p class="text-sm md:text-lg">{personalStatement}</p>
    </div>

    <!-- Timeline and Skills Section -->
    <div class="flex flex-col md:flex-row items-start">
        <div class="w-full md:w-1/2 md:pr-4">
            <h2 class="text-2xl md:text-4xl mb-4 font-bold">Timeline</h2>
            <Timeline/>

            <!-- Extracurricular Activities -->
            <div class="mb-10">
                <h2 class="text-2xl md:text-4xl mb-4 font-bold">Extracurricular Activities</h2>
                <div class="text-sm md:text-lg">
                    {#each extracurricularActivities as activity}
                        <div class="mb-4">
                            <div class="font-semibold text-lg md:text-xl">{activity.title}</div>
                            <p>{activity.description}</p>
                        </div>
                    {/each}
                </div>
            </div>
        </div>

        <!-- Vertical Divider -->
        <span class="hidden md:block border-l-2 border-gray-300 h-full mx-4"></span>

        <div class="w-full md:w-1/2 md:pl-4">
            <!-- Skills Section -->
            <div class="mb-10">
                <h2 class="text-2xl md:text-4xl mb-4 font-bold">Skills</h2>
                <ul class="text-sm md:text-xl list-disc list-inside">
                    {#each skills as skill}
                        <li class="mb-4 flex items-start">
                            <i class="fa-solid fa-gem text-lg md:text-xl mr-2"></i>
                            <div>
                                <div class="font-semibold text-lg md:text-xl">{skill.category}</div>
                                <p class="text-sm md:text-lg">{skill.items.join(", ")}</p>
                            </div>
                        </li>
                    {/each}
                </ul>
            </div>

            <!-- Projects Section -->
            <div class="mb-10">
                <h2 class="text-2xl md:text-4xl mb-4 font-bold">Projects</h2>
                <p class="text-sm md:text-lg">
                    I have worked on various personal and group projects.
                    More details can be found in the
                    <a href='/portfolio' class='hover:underline font-bold'>Portfolio</a>
                    section of my website.
                </p>
            </div>

            <!-- Certifications Section -->
            <div class="mb-10">
                <h2 class="text-2xl md:text-4xl mb-4 font-bold">Certifications</h2>
                <div class="text-sm md:text-lg">
                    {#each certifications as cert}
                        <div class="mb-6 flex items-start">
                            <i class="fa-solid fa-award text-lg md:text-2xl mr-2"></i>
                            <div>
                                <div class="font-semibold text-lg md:text-xl">{cert.title}</div>
                                <p class="text-sm md:text-md">{cert.description}</p>
                            </div>
                        </div>
                    {/each}
                </div>
            </div>
        </div>
    </div>
</div>
