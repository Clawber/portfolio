<script>
  import { Menu } from 'lucide-svelte';

  let showMobileMenu = false;
</script>

<header class="bg-navy/80 backdrop-blur-sm fixed top-0 left-0 right-0 z-50">
  <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
    <a href="/" class="text-2xl font-bold text-white hover:text-teal transition-colors">
      J.E.S.
    </a>
    
    <!-- Desktop Menu -->
    <div class="hidden md:flex space-x-8 items-center">
      <a href="#about" class="hover:text-teal transition-colors">About</a>
      <a href="#skills" class="hover:text-teal transition-colors">Skills</a>
      <a href="#projects" class="hover:text-teal transition-colors">Projects</a>
      <!-- <a href="#services" class="hover:text-teal transition-colors">Services</a> -->
      <a href="#contact" class="border border-teal text-teal px-4 py-2 rounded hover:bg-teal/10 transition-colors">Contact Me</a>
    </div>

    <!-- Mobile Menu Button -->
    <button on:click={() => showMobileMenu = !showMobileMenu} class="md:hidden">
      <Menu class="text-white" />
    </button>
  </nav>

  <!-- Mobile Menu -->
  {#if showMobileMenu}
    <div class="md:hidden bg-light-navy flex flex-col items-center space-y-4 py-4">
      <a href="#about" on:click={() => showMobileMenu = false} class="hover:text-teal transition-colors">About</a>
      <a href="#skills" on:click={() => showMobileMenu = false} class="hover:text-teal transition-colors">Skills</a>
      <a href="#projects" on:click={() => showMobileMenu = false} class="hover:text-teal transition-colors">Projects</a>
      <!-- <a href="#services" on:click={() => showMobileMenu = false} class="hover:text-teal transition-colors">Services</a> -->
      <a href="#contact" on:click={() => showMobileMenu = false} class="border border-teal text-teal px-4 py-2 rounded hover:bg-teal/10 transition-colors w-11/12 text-center">Contact Me</a>
    </div>
  {/if}
</header>