<script>
  import Accordion from '$lib/components/Accordion.svelte';
</script>

<div class="max-w-3xl mx-auto">
  <h1 class="text-4xl font-bold text-center mb-12">
    Mes Compétences
  </h1>

  <div class="mb-8 p-6 bg-white dark:bg-gray-800 rounded-lg shadow-md dark:border border-gray-700">
    <h2 class="text-2xl font-bold mb-2">Compétence 2 : Optimiser des applications</h2>
    <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">
      Sélectionner les algorithmes adéquats pour répondre à un problème donné
    </p>

    <Accordion title="AC 1 : Choisir des structures de données complexes">
      <p class="mb-2">Dans ce projet, j’ai dû faire des choix précis de structures de données pour répondre aux besoins de l’interface JavaFX et à la logique métier du système ferroviaire. L’enjeu principal était d'assurer un fonctionnement fluide et ergonomique, en organisant efficacement les informations (gares, trajets, horaires). Ce travail m’a permis d’appliquer une réflexion concrète sur l’adéquation entre les structures choisies et les contraintes du projet.</p>
      <a href="/ethan" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : La légende d’Éthane</a>
    </Accordion>

    <Accordion title="AC 2 : Utiliser des techniques algorithmiques adaptées">
      <p class="mb-2">Pour permettre aux trains de trouver le chemin le plus court entre deux gares, j’ai intégré l’algorithme de Dijkstra. Cela répondait à un problème d’optimisation de parcours dans un graphe. Le bon fonctionnement de cette recherche de chemin optimal était essentiel à la fluidité du système.</p>
      <a href="/trains" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : Trains</a>
    </Accordion>

    <Accordion title="AC 3 : Comprendre les enjeux de sécurisation">
      <p class="mb-2">Pour garantir la sécurité de la plateforme CTF, j’ai dû configurer correctement le serveur, restreindre l’accès à certaines ressources, et protéger les données stockées en base. Ce projet m’a permis de mettre en œuvre plusieurs bonnes pratiques en matière de sécurisation d’un système complet.</p>
      <a href="/ctfd" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : CTFd</a>
    </Accordion>

    <Accordion title="AC 4 : Évaluer l’impact environnemental et sociétal">
      <p class="mb-2">L’algorithme de Dijkstra permet de calculer les trajets les plus courts entre les gares. Dans ce jeu, l’impact environnemental est minime, mais dans un vrai projet ferroviaire, optimiser les parcours réduit la consommation d’énergie et améliore l’efficacité des transports, ce qui a un impact positif significatif.</p>
      <a href="/trains" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : Trains</a>
    </Accordion>
  </div>

  <div class="mb-8 p-6 bg-white dark:bg-gray-800 rounded-lg shadow-md dark:border border-gray-700">
    <h2 class="text-2xl font-bold mb-2">Compétence 3 : Administrer des systèmes complexes</h2>
    <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">
      Faire évoluer et maintenir un système informatique communicant en conditions opérationnelles
    </p>

    <Accordion title="AC 1 : Concevoir des applications communicantes">
      <p class="mb-2">J’ai conçu et développé l’application web CTFd en assurant la communication entre le serveur, la base de données et les clients, garantissant ainsi une expérience fluide et interactive pour les participants.</p>
      <a href="/ctfd" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : CTFd</a>
    </Accordion>

    <Accordion title="AC 2 : Utiliser des services réseaux virtualisés">
      <p class="mb-2">J’ai déployé l’application sur un serveur virtualisé, ce qui a permis une gestion flexible des ressources, une isolation des services et une meilleure scalabilité lors des compétitions.</p>
      <a href="/ctfd" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : CTFd</a>
    </Accordion>

    <Accordion title="AC 3 : Sécuriser les services et données d’un système">
      <p class="mb-2">J’ai mis en place des mécanismes de sécurité tels que l’authentification, le contrôle d’accès, et la sécurisation des communications pour protéger les données sensibles des utilisateurs et garantir la robustesse du système.</p>
      <a href="/ctfd" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : CTFd</a>
    </Accordion>
  </div>

  <div class="mb-8 p-6 bg-white dark:bg-gray-800 rounded-lg shadow-md dark:border border-gray-700">
    <h2 class="text-2xl font-bold mb-2">Compétence 4 : Gérer des données de l’information</h2>
    <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">
      Optimiser une base de données, interagir avec une application et mettre en œuvre la sécurité
    </p>

    <Accordion title="AC 1 : Optimiser les modèles de données">
      <p class="mb-2">J’ai conçu et optimisé la base de données relationnelle pour assurer des requêtes rapides et une gestion efficace des utilisateurs, des épreuves et des scores, tout en facilitant l’évolution future du système.</p>
      <a href="/ctfd" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : CTFd</a>
    </Accordion>

    <Accordion title="AC 2 : Assurer la confidentialité des données">
      <p class="mb-2">J’ai mis en œuvre des mesures de sécurité pour protéger les données personnelles des participants, incluant le chiffrement des mots de passe et des accès restreints aux informations sensibles.</p>
      <a href="/ctfd" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : CTFd</a>
    </Accordion>

    <Accordion title="AC 3 : Organiser la restitution de données">
      <p class="mb-2">Dans le jeu de plateforme Ethan, les coordonnées du personnage sont constamment calculées et utilisées pour afficher sa position, gérer les interactions avec l’environnement, et ajuster la caméra. Cette restitution en temps réel des données positionnelles est essentielle pour offrir une expérience de jeu fluide et réactive.</p>
      <a href="/ethan" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : La légende d’Éthane</a>
    </Accordion>

    <Accordion title="AC 4 : Manipuler des données hétérogènes">
      <p class="mb-2">Le projet intègre différentes sources et formats de données (logs, bases relationnelles, fichiers de configuration), que j’ai su manipuler et harmoniser pour assurer la cohérence globale.</p>
      <a href="/ctfd" class="text-blue-600 dark:text-blue-400 hover:underline text-sm font-medium">Voir le projet : CTFd</a>
    </Accordion>
  </div>
</div>