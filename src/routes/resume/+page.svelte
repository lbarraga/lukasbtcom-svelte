<script>
    import Timeline from "./Timeline.svelte";
    import profilePic from "$lib/images/me-casual.jpg";
    import { Avatar } from "@skeletonlabs/skeleton";

    import resume from "$lib/data/resume.json";
    import skills from "$lib/data/skills.json";
    import IconedListItem from "./IconedListItem.svelte";
</script>

<div class="variant-ghost-surface w-full md:w-3/5 mx-auto p-4 md:p-10">

    <!-- Profile Picture and Heading -->
    <div class="flex flex-col md:flex-row mb-10">
        <Avatar src={profilePic} rounded="rounded-xl" class="mb-4 md:mb-0 md:mr-4 w-44"/>
        <div>
            <h1 class="text-3xl md:text-5xl mb-2 font-extrabold">
                {resume.profile.name}
            </h1>
            <p class="text-xl md:text-2xl">
                {resume.profile.title}
            </p>

            <div class="flex flex-col mt-4">
                {#each resume.profile.links as link}
                    <div class="flex items-center mb-2">
                        <i class="iconify text-lg md:text-xl mr-2" data-icon={link.icon}></i>
                        <a href={link.link} class="text-sm md:text-lg hover:underline" target="_blank">{link.text}</a>
                    </div>
                {/each}
            </div>
        </div>
    </div>

    <!-- Personal Statement -->
    <div class="mb-10">
        <h2 class="text-2xl md:text-4xl mb-4 font-bold">{resume.personalStatement.title}</h2>
        <p class="md:text-lg">{resume.personalStatement.content}</p>
    </div>

    <!-- Grid Layout with Two Columns -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">

        <!-- Timeline -->
        <div>
            <h2 class="text-2xl md:text-4xl mb-4 font-bold">{resume.timeline.title}</h2>
            <Timeline/>
        </div>

        <!-- Skills Section -->
        <div>
            <h2 class="text-2xl md:text-4xl mb-4 font-bold">{resume.skills.title}</h2>
            <ul class="space-y-5">
                {#each skills.skills as skill}
                    <IconedListItem
                            icon="fluent-emoji-high-contrast:gem-stone"
                            title={skill.skill}
                            content={skill.technologies.map(t => t.name).join(', ')}
                    />
                {/each}
            </ul>
        </div>

        <div>
            <!-- Certifications Section -->
            <div class="mb-10">
                <h2 class="text-2xl md:text-4xl mb-4 font-bold">{resume.certifications.title}</h2>
                <ul class="space-y-5">
                    {#each resume.certifications.content as cert}
                        <IconedListItem
                                icon="ph:certificate"
                                title={cert.title}
                                content={cert.description}
                        />
                    {/each}
                </ul>
            </div>

            <!-- Projects Section -->
            <div>
                <h2 class="text-2xl md:text-4xl mb-4 font-bold">Projects</h2>
                <p class="text-sm md:text-lg mb-10">
                    I have worked on various personal and group projects.
                    More details can be found in the
                    <a href='/portfolio' class='hover:underline font-bold'>Portfolio</a>
                    section of my website.
                </p>
            </div>

        </div>

        <!-- Extracurricular Activities -->
        <div>
            <h2 class="text-2xl md:text-4xl mb-4 font-bold">{resume.extracurricular.title}</h2>
            <ul class="space-y-4">
                {#each resume.extracurricular.content as activity}
                    <IconedListItem
                            icon="fluent-emoji-high-contrast:gem-stone"
                            title={activity.title}
                            content={activity.description}
                    />
                {/each}
            </ul>
        </div>



    </div>
</div>
