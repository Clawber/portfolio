<script>
    import ProjectCard from '../ProjectCard.svelte';
    
    const projects = [
        {
            title: "SmokeTrace – Real-Time IoT Smoke Monitoring Platform",
            description: "An end-to-end IoT system that tracks smoke levels in real time, with a custom frontend, backend, and scalable systems architecture for live data monitoring.",
            tech: ["SvelteKit", "Node.js", "PostgreSQL", "Firebase", "Deno"],
            link: "https://github.com/your-username/project-one"
        },
        {
            title: "Jeeps – Real-Time Fleet Tracking for Philippine Jeepneys",
            description: "A GPS-based fleet tracking system with real-time location updates and a responsive user interface for monitoring public transport vehicles.",
            tech: ["Svelte", "Node.js", "Postgresql", "MongoDB"],
            link: "https://github.com/your-username/project-two"
        },
        {
            title: "Gemma – AI-Powered Learning Platform for Students",
            description: "An AI-driven learning platform that personalizes content and adapts to student performance through intelligent recommendations and data analytics.",
            tech: ["SvelteKit", "Node.js", "Gemini API"],
            link: "https://github.com/your-username/project-three"
        },
        // {
        //     title: "Time Series Analysis",
        //     description: "An analytics dashboard that fetches and displays complex data sets in interactive charts and graphs.",
        //     tech: ["SvelteKit", "D3.js", "Tailwind CSS", "REST API"],
        //     link: "https://github.com/your-username/project-three"
        // }
    ];
</script>

<section id="projects" class="py-20 md:py-32 container mx-auto px-6">
    <h2 class="text-3xl font-bold text-lightest-slate mb-12 flex items-center">
        <span class="text-teal font-mono mr-4 text-2xl">03.</span> Things I've Built
        <span class="ml-6 h-px w-32 bg-lightest-navy"></span>
    </h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        {#each projects as project}
            <ProjectCard {...project} />
        {/each}
    </div>
</section>