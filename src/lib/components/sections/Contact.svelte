<script>
    import { Github, Linkedin } from 'lucide-svelte';
</script>

<section id="contact" class="py-20 md:py-32 text-center container mx-auto px-6">
    <h2 class="font-mono text-teal mb-2">05. What's Next?</h2>
    <h3 class="text-5xl font-bold text-lightest-slate mb-4">Get In Touch</h3>
    <p class="max-w-xl mx-auto mb-8">
        I'm actively seeking new opportunities and I'm always open to discussing new projects. Whether you have a question or just want to say hi, I'll do my best to get back to you!
    </p>

    <a href="mailto:johnerick.sarenas@email.com" class="inline-block bg-transparent border border-teal text-teal font-mono text-lg py-3 px-8 rounded hover:bg-teal/10 transition-all duration-300">
        Say Hello
    </a>

    <div class="flex justify-center space-x-6 mt-16">
        <a href="https://github.com/your-username" target="_blank" rel="noopener noreferrer" class="hover:text-teal transition-colors">
            <Github size={24} />
        </a>
        <a href="https://linkedin.com/in/your-username" target="_blank" rel="noopener noreferrer" class="hover:text-teal transition-colors">
            <Linkedin size={24} />
        </a>
    </div>
</section>