<script>
  import { onMount } from 'svelte';
  import Typed from 'typed.js';

  onMount(() => {
    const options = {
      strings: [
        "Je m'appelle Omer Tilki",
        "Développeur Backend & Data",
        "Actuellement étudiant"
      ],
      typeSpeed: 70,
      backSpeed: 40,
      loop: true,
      smartBackspace: true
    };
    // @ts-ignore
    const typed = new Typed('#typed-element', options);

    return () => {
      typed.destroy();
    };
  });
</script>

<section class="min-h-[70vh] flex flex-col-reverse lg:flex-row items-center gap-12">

  <div class="lg:w-2/3">
    <h1 class="text-4xl sm:text-6xl font-bold tracking-tighter mb-4">
      Bonjour,
    </h1>
    <div class="text-2xl sm:text-3xl text-gray-600 dark:text-gray-300 min-h-[80px]">
      <span id="typed-element"></span>
    </div>
    <p class="mt-6 text-lg text-gray-700 dark:text-gray-400">
      Bienvenue sur mon portfolio. Je suis un développeur spécialisé dans l'intégration
      d'applications et le management du système d'information.
    </p>
  </div>

  <div class="lg:w-1/3 flex-shrink-0">
    <img
      src="/profil2.jpg"
      alt="Omer Tilki"
      class="w-64 h-64 lg:w-80 lg:h-80 object-cover rounded-full shadow-lg mx-auto"
    >
  </div>
</section>

<section class="mt-24">
  <h2 class="text-3xl font-bold text-center mb-12">
    Mes Projets
  </h2>

  <div class="grid md:grid-cols-3 gap-8">
    <a href="/ethan" class="block p-6 bg-white dark:bg-gray-800 rounded-lg shadow-md hover:shadow-xl transition-shadow dark:border border-gray-700">
      <h3 class="text-2xl font-bold mb-2">La légende d’Éthane</h3>
      <p class="text-gray-600 dark:text-gray-400">Un premier jeu vidéo crée avec passion en C# et Unity.</p>
    </a>
    <a href="/trains" class="block p-6 bg-white dark:bg-gray-800 rounded-lg shadow-md hover:shadow-xl transition-shadow dark:border border-gray-700">
      <h3 class="text-2xl font-bold mb-2">Trains</h3>
      <p class="text-gray-600 dark:text-gray-400">Adaptation numérique d'un jeu de société japonais en Java/JavaFX.</p>
    </a>
    <a href="/ctfd" class="block p-6 bg-white dark:bg-gray-800 rounded-lg shadow-md hover:shadow-xl transition-shadow dark:border border-gray-700">
      <h3 class="text-2xl font-bold mb-2">CTFd</h3>
      <p class="text-gray-600 dark:text-gray-400">Création d'un "Capture The Flag" avec Docker, Flask et MariaDB.</p>
    </a>
  </div>
</section>