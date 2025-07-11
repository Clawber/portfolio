<script>
  import Header from '$lib/components/Header.svelte';
  import Hero from '$lib/components/sections/Hero.svelte';
  import About from '$lib/components/sections/About.svelte';
  import Skills from '$lib/components/sections/Skills.svelte';
  import Projects from '$lib/components/sections/Projects.svelte';
  // import Services from '$lib/components/sections/Services.svelte'; test commit
  import Contact from '$lib/components/sections/Contact.svelte';
</script>

<Header />

<main class="flex flex-col bg-black">
    <Hero />
    <About />
    <Skills />
    <Projects />
    <!-- <Services /> -->
    <Contact />
</main>

<footer class="text-center py-6 text-sm text-slate bg-neutral-800">
    <p>Designed & Built by John Erick Sarenas</p>
</footer>

<style>
  /* This enables smooth scrolling for anchor links */
  :global(html) {
    scroll-behavior: smooth;
  }
</style>