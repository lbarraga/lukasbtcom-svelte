<script>
    import Timeline from "./Timeline.svelte";
    import profilePic from "$lib/images/me-casual.jpg";
    import { Avatar } from "@skeletonlabs/skeleton";

    import resume from "$lib/data/resume.json";
    import skills from "$lib/data/skills.json";
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
        <p class="text-sm md:text-lg">{resume.personalStatement.content}</p>
    </div>

    <div class="flex flex-col md:flex-row items-start">

        <!-- Left side -->
        <div class="w-full md:w-1/2 md:pr-4">

            <!-- Timeline -->
            <h2 class="text-2xl md:text-4xl mb-4 font-bold">{resume.timeline.title}</h2>
            <Timeline/>

            <!-- Extracurricular Activities -->
            <div class="mb-10">
                <h2 class="text-2xl md:text-4xl mb-4 font-bold">{resume.extracurricular.title}</h2>
                <div class="text-sm md:text-lg">
                    {#each resume.extracurricular.content as activity}
                        <div class="mb-4">
                            <div class="font-semibold text-lg md:text-xl">{activity.title}</div>
                            <p>{activity.description}</p>
                        </div>
                    {/each}
                </div>
            </div>
        </div>

        <!-- Right side -->
        <div class="w-full md:w-1/2 md:pl-4">

            <!-- Skills Section -->
            <div class="mb-10">
                <h2 class="text-2xl md:text-4xl mb-4 font-bold">{resume.skills.title}</h2>
                <ul class="text-sm md:text-xl list-disc list-inside">
                    {#each skills.skills as skill}
                        <li class="mb-4 flex items-start">
                            <i class="iconify text-sm mr-2 mt-2" data-icon="fa-solid:gem"></i>

                            <div>
                                <div class="font-semibold text-lg md:text-xl">{skill.skill}</div>
                                <p class="text-sm md:text-lg">
                                    {skill.technologies.map(t => t.name).join(', ')}
                                </p>
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
                <h2 class="text-2xl md:text-4xl mb-4 font-bold">{resume.certifications.title}</h2>
                <div class="text-sm md:text-lg">
                    {#each resume.certifications.content as cert}
                        <div class="mb-6">
                            <div class="flex items-center ">
                                <i class="iconify mr-2 text-2xl" data-icon="ph:certificate"></i>
                                <h2 class="font-semibold">
                                    {cert.title}
                                </h2>
                            </div>
                            <p>{cert.description}</p>
                        </div>
                    {/each}
                </div>
            </div>


        </div>
    </div>
</div>
