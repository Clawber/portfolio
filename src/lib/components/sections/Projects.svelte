<script>
    import ProjectCard from '../ProjectCard.svelte';
    
    const projects = [
        {
            title: "E-Commerce Platform",
            description: "A full-featured online store with a custom CMS, payment integration, and a responsive user interface.",
            tech: ["SvelteKit", "Node.js", "PostgreSQL", "Stripe API"],
            link: "https://github.com/your-username/project-one"
        },
        {
            title: "Real-Time Chat Application",
            description: "A scalable chat app using WebSockets for instant messaging and presence indicators.",
            tech: ["Svelte", "Express", "Socket.io", "MongoDB"],
            link: "https://github.com/your-username/project-two"
        },
        {
            title: "Data Visualization Dashboard",
            description: "An analytics dashboard that fetches and displays complex data sets in interactive charts and graphs.",
            tech: ["SvelteKit", "D3.js", "Tailwind CSS", "REST API"],
            link: "https://github.com/your-username/project-three"
        }
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