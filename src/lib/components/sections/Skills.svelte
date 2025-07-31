<script>
    import { Code, Database, Settings, Cloud, Users } from 'lucide-svelte';
</script>

<section id="skills" class="py-20 md:py-32 container mx-auto px-6">
    <h2 class="text-3xl font-bold text-lightest-slate mb-12 flex items-center justify-center">
        <span class="text-teal font-mono mr-4 text-2xl">02.</span> My Tech Stack
    </h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 text-center">
        
        <!-- Programming Languages -->
        <div class="bg-light-navy p-6 rounded-lg">
            <Code class="mx-auto text-teal mb-4" size={48} />
            <h3 class="text-xl font-bold text-lightest-slate mb-2">Programming Languages</h3>
            <p class="font-mono text-slate">Python, JavaScript, Svelte, HTML5, CSS3</p>
        </div>

        <!-- Frameworks & Libraries -->
        <div class="bg-light-navy p-6 rounded-lg">
            <Settings class="mx-auto text-teal mb-4" size={48} />
            <h3 class="text-xl font-bold text-lightest-slate mb-2">Frameworks & Libraries</h3>
            <p class="font-mono text-slate">SvelteKit, React.js, Node.js, Express.js, Tailwind CSS</p>
        </div>

        <!-- Databases -->
        <div class="bg-light-navy p-6 rounded-lg">
            <Database class="mx-auto text-teal mb-4" size={48} />
            <h3 class="text-xl font-bold text-lightest-slate mb-2">Databases</h3>
            <p class="font-mono text-slate">PostgreSQL, MongoDB, SQL</p>
        </div>

        <!-- Tools & Platforms -->
        <div class="bg-light-navy p-6 rounded-lg">
            <Cloud class="mx-auto text-teal mb-4" size={48} />
            <h3 class="text-xl font-bold text-lightest-slate mb-2">Tools & Platforms</h3>
            <p class="font-mono text-slate">Git, GitHub, AWS, Docker, Vercel</p>
        </div>







        <!-- Soft Skills -->
        <div class="bg-light-navy p-6 rounded-lg md:col-span-2 lg:col-span-1">
             <Users class="mx-auto text-teal mb-4" size={48} />
             <h3 class="text-xl font-bold text-lightest-slate mb-2">Soft Skills</h3>
             <p class="font-mono text-slate">Problem-Solving, Communication, Agile</p>
        </div>
    </div>
</section>