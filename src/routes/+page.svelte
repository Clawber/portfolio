<script>
    import Navbar from "$lib/Navbar.svelte";

    const services = [
      {
        id: 1,
        logo: '🎨', // Use an emoji or replace with actual image paths later
        title: 'Web Design',
        description: 'Crafting stunning and intuitive user interfaces that capture your brand\'s essence.',
        altText: 'Design palette icon'
      },
      {
        id: 2,
        logo: '💻', // Example: 'path/to/development-icon.svg'
        title: 'Web Development',
        description: 'Building robust, scalable, and high-performance websites and web applications.',
        altText: 'Laptop and code icon'
      },
      {
        id: 3,
        logo: '📊', // Example: 'path/to/seo-icon.svg'
        title: 'SEO & Marketing',
        description: 'Optimizing your online presence to reach a wider audience and drive organic growth.',
        altText: 'Chart icon'
      },
      {
        id: 4,
        logo: '💡',
        title: 'Consulting',
        description: 'Providing expert guidance and strategic insights to achieve your digital goals.',
        altText: 'Lightbulb icon'
      },
      {
        id: 5,
        logo: '📱',
        title: 'Mobile Apps',
        description: 'Developing user-friendly and feature-rich mobile applications for iOS and Android.',
        altText: 'Mobile phone icon'
      }
    ];

    // A simple way to group services into "carousel components" of 3
    // For a real carousel, you'd implement proper prev/next or dot navigation.
    // Here, each 'carousel' will simply display 3 cards.
    const serviceGroups = [];
    for (let i = 0; i < services.length; i += 3) {
      serviceGroups.push(services.slice(i, i + 3));
    }
</script>

<Navbar />

<section class="min-h-screen bg-gradient-to-r from-gray-900 to-gray-700 text-white py-16 md:py-24 lg:py-32">
  <div class="container mx-auto px-4 flex flex-col md:flex-row items-center justify-between gap-12">

    <div class="w-full md:w-1/2 text-center md:text-left">
      <h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-extrabold leading-tight mb-4 drop-shadow-lg">
        Unlock Your Creative <span class="text-blue-400">Potential</span>
      </h1>
      <p class="text-lg sm:text-xl md:text-2xl text-gray-300 mb-8 max-w-xl mx-auto md:mx-0">
        Discover powerful tools and resources to bring your ideas to life. From design to development, we've got you covered.
      </p>
      <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
        <a
          href="/get-started"
          class="px-8 py-3 bg-blue-600 hover:bg-blue-700 text-white font-semibold rounded-full shadow-lg transition duration-300 ease-in-out transform hover:scale-105"
        >
          Get Started Now
        </a>
        <a
          href="/learn-more"
          class="px-8 py-3 bg-transparent border-2 border-blue-400 text-blue-400 hover:bg-blue-400 hover:text-white font-semibold rounded-full shadow-lg transition duration-300 ease-in-out transform hover:scale-105"
        >
          Learn More
        </a>
      </div>
    </div>

    <div class="w-full md:w-1/2 flex justify-center md:justify-end">
      <img
        src="https://images.unsplash.com/photo-1596556101915-d41c1071d79e?auto=format&fit=crop&q=80&w=2940&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="Creative workspace with laptop and design elements"
        class="rounded-lg shadow-2xl max-w-full h-auto object-cover max-h-[500px] w-auto animate-fade-in-up"
      />
    </div>

  </div>
</section>

<section class="bg-gray-50 py-16 md:py-24">
  <div class="container mx-auto px-4">
    <h2 class="text-4xl sm:text-5xl md:text-6xl font-extrabold text-center text-gray-900 mb-12 drop-shadow-md">
      My Expert Services
    </h2>

    <div class="grid grid-cols-1 gap-8 lg:gap-12">
      {#each serviceGroups as group, groupIndex}
        <div class="bg-white rounded-xl shadow-xl p-8 transform transition-all duration-300 hover:scale-[1.02]">
          <h3 class="text-3xl font-bold text-gray-800 mb-6 text-center">
            Service Category {groupIndex + 1}
          </h3>
          <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            {#each group as service (service.id)}
              <div class="text-center p-6 bg-blue-50 rounded-lg shadow-md hover:shadow-lg transition-shadow duration-200">
                <div class="text-5xl mb-4" aria-label={service.altText}>
                  {service.logo}
                </div>
                <h4 class="text-xl font-semibold text-gray-800 mb-2">{service.title}</h4>
                <p class="text-gray-600 text-sm">{service.description}</p>
              </div>
            {/each}
          </div>
        </div>
      {/each}

      </div>
  </div>
</section>

<style lang="postcss">
  /*
    Define a simple fade-in animation for the image.
    Add this to your main app.css or directly in this component's style block.
  */
  @reference "tailwindcss";

  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .animate-fade-in-up {
    animation: fadeInUp 0.8s ease-out forwards;
    animation-delay: 0.3s; /* Delay the animation slightly after content appears */
    opacity: 0; /* Start hidden */
  }
</style>