<script>
  import Navbar from '$lib/components/Navbar.svelte';
  import '../app.css'; // Fichier principal de Tailwind
</script>

<div class="bg-gray-50 dark:bg-gray-900 text-gray-900 dark:text-gray-100 min-h-screen transition-colors duration-300">

  <Navbar />

  <main class="container mx-auto max-w-5xl p-6 pt-24 sm:pt-32">
    <slot />
  </main>

  <footer class="text-center p-10 text-gray-500 text-sm">
    Omer Tilki © {new Date().getFullYear()}
  </footer>
</div>