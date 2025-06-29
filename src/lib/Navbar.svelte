<script>
  import { fade } from 'svelte/transition';

  let isOpen = false; // State to control mobile menu visibility

  // Function to toggle the mobile menu
  function toggleMenu() {
    isOpen = !isOpen;
  }
</script>

<nav class="bg-gray-800 p-4 shadow-lg">
  <div class="container mx-auto flex items-center justify-between flex-wrap">
    <a href="/" class="text-white text-2xl font-bold tracking-wider">
      YourLogo
    </a>

    <div class="block lg:hidden">
      <button
        on:click={toggleMenu}
        class="flex items-center px-3 py-2 border rounded text-gray-200 border-gray-400 hover:text-white hover:border-white"
        aria-label="Toggle navigation"
      >
        <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/>
        </svg>
      </button>
    </div>

    <div class="hidden lg:flex flex-grow items-center justify-end">
      <div class="text-sm lg:flex-grow">
        <a href="/home" class="block mt-4 lg:inline-block lg:mt-0 text-gray-300 hover:text-white mr-6">
          Home
        </a>
        <a href="/about" class="block mt-4 lg:inline-block lg:mt-0 text-gray-300 hover:text-white mr-6">
          About
        </a>
        <a href="/services" class="block mt-4 lg:inline-block lg:mt-0 text-gray-300 hover:text-white mr-6">
          Services
        </a>
        <a href="/contact" class="block mt-4 lg:inline-block lg:mt-0 text-gray-300 hover:text-white">
          Contact
        </a>
      </div>
      <div>
        <a href="/login" class="inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-gray-800 hover:bg-white mt-4 lg:mt-0">
          Login
        </a>
      </div>
    </div>

    {#if isOpen}
      <div
        transition:fade={{ duration: 150 }}
        class="w-full block flex-grow lg:hidden mt-4 text-center"
      >
        <a href="/home" class="block text-gray-300 hover:text-white py-2">
          Home
        </a>
        <a href="/about" class="block text-gray-300 hover:text-white py-2">
          About
        </a>
        <a href="/services" class="block text-gray-300 hover:text-white py-2">
          Services
        </a>
        <a href="/contact" class="block text-gray-300 hover:text-white py-2">
          Contact
        </a>
        <div class="mt-4">
          <a href="/login" class="inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-gray-800 hover:bg-white">
            Login
          </a>
        </div>
      </div>
    {/if}
  </div>
</nav>

<style lang="postcss">
  /*
    PostCSS is enabled by svelte-add tailwindcss,
    so you can use @apply if you want to extract common styles,
    though for a simple navbar, direct Tailwind classes are often sufficient.
  */
</style>