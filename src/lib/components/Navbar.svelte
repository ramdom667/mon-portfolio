<script>
  import { base } from '$app/paths';
  import ThemeToggle from '$lib/components/ThemeToggle.svelte';
  import LangToggle from '$lib/components/LangToggle.svelte';
  import { page } from '$app/stores';

  const navLinks = [
    { href: `${base}/`, text: 'Accueil' },
    { href: `${base}/ethan`, text: 'Ethan' },
    { href: `${base}/trains`, text: 'Trains' },
    { href: `${base}/ctfd`, text: 'CTFd' },
    { href: `${base}/competences`, text: 'Compétences' },
    { href: `${base}/a-propos`, text: 'À Propos' },
  ];
</script>

<nav
  class="fixed top-0 left-0 right-0 z-50 bg-gray-50/80 dark:bg-gray-900/80 backdrop-blur-md border-b border-gray-200 dark:border-gray-800">
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
      </div>
    </div>
  </div>
</nav>