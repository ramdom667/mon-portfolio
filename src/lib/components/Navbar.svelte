<script>
  import { base } from '$app/paths';
  import ThemeToggle from '$lib/components/ThemeToggle.svelte';
  import LangToggle from '$lib/components/LangToggle.svelte';
  import { page } from '$app/stores';

  let isMenuOpen = false;

  const navLinks = [
    { href: `${base}/`, text: 'Accueil' },
    { href: `${base}/ethan`, text: 'Ethan' },
    { href: `${base}/trains`, text: 'Trains' },
    { href: `${base}/ctfd`, text: 'CTFd' },
    { href: `${base}/a-propos`, text: 'À Propos' },
    { href: `${base}/competences`, text: 'Compétences' },
  ];

  function toggleMenu() {
    isMenuOpen = !isMenuOpen;
  }
</script>

<nav class="fixed top-0 left-0 right-0 z-50 bg-gray-50/80 dark:bg-gray-900/80 backdrop-blur-md border-b border-gray-200 dark:border-gray-800">
  <div class="container mx-auto max-w-5xl px-6 py-4">
    <div class="flex justify-between items-center">
      <a href="{base}/" class="text-xl font-bold tracking-tight hover:text-blue-600 transition-colors">
        Omer Tilki
      </a>

      <div class="hidden md:flex space-x-6">
        {#each navLinks as link (link.href)}
          <a
            href={link.href}
            class="text-sm font-medium {$page.url.pathname === link.href
              ? 'text-blue-600 dark:text-blue-400'
              : 'text-gray-600 dark:text-gray-300 hover:text-black dark:hover:text-white'}"
          >
            {link.text}
          </a>
        {/each}
      </div>

      <div class="flex items-center space-x-3">
        <LangToggle />
        <ThemeToggle />

        <button
          on:click={toggleMenu}
          class="md:hidden p-2 rounded-md hover:bg-gray-200 dark:hover:bg-gray-700 focus:outline-none"
        >
          <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            {#if isMenuOpen}
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            {:else}
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            {/if}
          </svg>
        </button>
      </div>
    </div>

    {#if isMenuOpen}
      <div class="md:hidden mt-4 pb-4 space-y-2">
        {#each navLinks as link (link.href)}
          <a
            href={link.href}
            on:click={() => isMenuOpen = false}
            class="block text-base font-medium p-2 rounded-md {$page.url.pathname === link.href
              ? 'text-blue-600 bg-blue-50 dark:bg-blue-900/20'
              : 'text-gray-600 dark:text-gray-300 hover:bg-gray-100 dark:hover:bg-gray-800'}"
          >
            {link.text}
          </a>
        {/each}
      </div>
    {/if}
  </div>
</nav>