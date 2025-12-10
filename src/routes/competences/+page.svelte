<script>
  import Accordion from '$lib/components/Accordion.svelte';
</script>

<div class="max-w-3xl mx-auto">
  <h1 class="text-4xl font-bold text-center mb-12">
    Mes Compétences
  </h1>

  <div class="mb-8 p-6 bg-white dark:bg-gray-800 rounded-lg shadow-md dark:border border-gray-700">
    <h2 class="text-2xl font-bold mb-2">Optimiser des applications</h2>
    <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">
      Sélectionner les algorithmes adéquats pour répondre à un problème donné
    </p>

    <Accordion title="AC 1 : Choisir des structures de données complexes">
      <p class="mb-2">J’ai dû faire des choix précis de structures de données pour répondre aux besoins de l’interface JavaFX et à la logique métier du système ferroviaire.</p>
      <a href="/ethan" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : La légende d’Éthane</a>
    </Accordion>

    <Accordion title="AC 2 : Utiliser des techniques algorithmiques">
      <p class="mb-2">Pour permettre aux trains de trouver le chemin le plus court entre deux gares, j’ai intégré l’algorithme de Dijkstra.</p>
      <a href="/trains" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : Trains</a>
    </Accordion>

    <Accordion title="AC 3 : Sécurisation des données">
      <p class="mb-2">Configuration du serveur, restriction des accès et protection des données stockées en base.</p>
      <a href="/ctfd" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : CTFd</a>
    </Accordion>
  </div>

  <div class="mb-8 p-6 bg-white dark:bg-gray-800 rounded-lg shadow-md dark:border border-gray-700">
    <h2 class="text-2xl font-bold mb-2">Administrer des systèmes complexes</h2>
    <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">
      Faire évoluer et maintenir un système informatique
    </p>

    <Accordion title="AC 1 : Concevoir des applications communicantes">
      <p class="mb-2">Conception de l’application web CTFd en assurant la communication fluide entre le serveur, la base de données et les clients.</p>
      <a href="/ctfd" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : CTFd</a>
    </Accordion>
  </div>

  <div class="mb-8 p-6 bg-white dark:bg-gray-800 rounded-lg shadow-md dark:border border-gray-700">
    <h2 class="text-2xl font-bold mb-2">Gérer des données de l’information</h2>
     <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">
      Optimiser une base de données et interagir avec une application
    </p>

    <Accordion title="AC 1 : Optimiser les modèles de données">
      <p class="mb-2">Conception et optimisation de la base de données relationnelle pour assurer des requêtes rapides.</p>
      <a href="/ctfd" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : CTFd</a>
    </Accordion>
  </div>
</div>