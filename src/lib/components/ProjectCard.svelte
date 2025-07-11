<script>
    import { Github, ExternalLink } from 'lucide-svelte';
    export let title, description, tech, link;
</script>

<div class="bg-light-navy p-6 rounded-lg flex flex-col h-full hover:-translate-y-2 transition-transform duration-300 shadow-lg">
    <div class="flex justify-between items-start mb-4">
        <h3 class="text-xl font-bold text-lightest-slate hover:text-teal transition-colors">
            <a href={link} target="_blank" rel="noopener noreferrer">{title}</a>
        </h3>
        <div class="flex space-x-3">
             <a href={link} target="_blank" rel="noopener noreferrer" class="hover:text-teal"><Github /></a>
             <a href={link} target="_blank" rel="noopener noreferrer" class="hover:text-teal"><ExternalLink /></a>
        </div>
    </div>
    <p class="text-light-slate flex-grow mb-4">{description}</p>
    <div class="flex flex-wrap gap-2 font-mono text-sm text-slate">
        {#each tech as item}
            <span>{item}</span>
        {/each}
    </div>
</div>