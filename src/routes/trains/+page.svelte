<script>
  import { base } from '$app/paths';

  const techStack = [
    { name: 'Java', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg' },
    { name: 'JavaFX', logo: 'https://raw.githubusercontent.com/luca-fabbian/devicons/master/icons/javafx/javafx-original.svg' },
    { name: 'Maven', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/maven/maven-original.svg' }
  ];
</script>

<div class="max-w-4xl mx-auto px-6 py-12 space-y-16">

  <header class="text-center space-y-4">
    <div class="inline-block px-3 py-1 bg-green-100 dark:bg-green-900/30 text-green-700 dark:text-green-300 rounded-full text-xs font-bold uppercase tracking-widest">
      Projet Académique • BUT Informatique
    </div>
    <h1 class="text-4xl md:text-6xl font-black tracking-tighter uppercase italic">
      TRAINS
    </h1>
    <p class="text-xl text-gray-500 italic">De la stratégie sur plateau à l'architecture logicielle Java.</p>
  </header>

  <div class="rounded-3xl overflow-hidden shadow-xl border border-gray-200 dark:border-gray-800 bg-white group">
    <img
      src="{base}/Trains-inter.png"
      alt="Interface du jeu Trains"
      class="w-full h-auto transition-transform duration-700 group-hover:scale-105"
    />
  </div>

  <section class="grid md:grid-cols-3 gap-12">
    <div class="md:col-span-2 space-y-8">
      <div class="space-y-4">
        <h2 class="text-2xl font-bold flex items-center gap-2">
          <span class="w-1.5 h-6 bg-green-600 rounded-full"></span>
          Conception & Logique
        </h2>
        <div class="text-gray-700 dark:text-gray-300 leading-relaxed space-y-4 text-lg">
          <p>
            Ce projet consistait à développer une version numérique complète du jeu de plateau japonais <strong>Trains</strong>.
            Le défi technique résidait dans la gestion d'un moteur de jeu complexe impliquant du <strong>Deck Building</strong>
            et de l'expansion de réseau ferroviaire.
          </p>
          <p>
            L'architecture logicielle repose sur une implémentation rigoureuse du pattern <strong>Modèle-Vue-Contrôleur (MVC)</strong>
            et d'une <strong>machine à états</strong> pour gérer les phases de jeu (Initialisation, Tour Normal, Pose de Rails).
            L'algorithme de <strong>Dijkstra</strong> a été intégré pour le calcul dynamique des scores basés sur la connectivité du réseau.
          </p>
        </div>
      </div>

      <div class="bg-gray-900 rounded-2xl p-6 border border-gray-800 shadow-inner">
        <div class="flex justify-between items-start mb-4">
          <div>
            <h4 class="text-green-400 font-bold text-sm">Algorithmique & Graphes</h4>
            <p class="text-gray-500 text-xs">Calcul des chemins les plus courts et gestion des tuiles.</p>
          </div>
          <div class="flex gap-1.5">
            <div class="w-2.5 h-2.5 rounded-full bg-red-500/20"></div>
            <div class="w-2.5 h-2.5 rounded-full bg-yellow-500/20"></div>
            <div class="w-2.5 h-2.5 rounded-full bg-green-500/20"></div>
          </div>
        </div>
        <code class="text-blue-300 text-xs font-mono">
          // Implémentation du parcours de graphe pour la connectivité des gares<br>
          public List&lt;Tuile&gt; calculerCheminPlusCourt(Gare source, Gare cible) &#123; ... &#125;
        </code>
      </div>
    </div>

    <aside class="space-y-8">
      <div class="p-6 bg-gray-50 dark:bg-gray-800/50 rounded-3xl border border-gray-100 dark:border-gray-700">
        <h3 class="text-xs font-black uppercase tracking-widest text-gray-400 mb-6 text-center">Environnement</h3>
        <div class="flex flex-col gap-3">
          {#each techStack as tech}
            <div class="flex items-center justify-between px-4 py-3 bg-white dark:bg-gray-900 rounded-xl border border-gray-100 dark:border-gray-800 shadow-sm">
              <span class="font-bold text-sm">{tech.name}</span>
              <img src={tech.logo} alt={tech.name} class="w-6 h-6" />
            </div>
          {/each}
        </div>
      </div>

      <div class="p-6 bg-green-50 dark:bg-green-900/10 rounded-3xl border border-green-100 dark:border-green-900/30">
        <h3 class="text-xs font-black uppercase tracking-widest text-green-600 mb-4 text-center">Compétences Clés</h3>
        <ul class="text-sm space-y-3 font-medium text-gray-700 dark:text-gray-300">
          <li class="flex items-center gap-2 underline decoration-green-500/30">Programmation Orientée Objet</li>
          <li class="flex items-center gap-2 underline decoration-green-500/30">Gestion d'IHM (JavaFX)</li>
          <li class="flex items-center gap-2 underline decoration-green-500/30">Architecture State Pattern</li>
          <li class="flex items-center gap-2 underline decoration-green-500/30">Algorithmique de Graphes</li>
        </ul>
      </div>
    </aside>
  </section>

  <footer class="text-center pt-8">
    <a
      href="https://github.com/ramdom667/trains-ihm"
      target="_blank"
      class="inline-flex items-center gap-4 px-10 py-4 bg-gray-900 dark:bg-gray-100 text-white dark:text-gray-900 rounded-2xl font-bold transition-all hover:scale-105 shadow-2xl"
    >
      <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current" xmlns="http://www.w3.org/2000/svg"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
      Explorer le code sur GitHub
    </a>
    <p class="text-[10px] text-gray-400 mt-4 uppercase tracking-[0.3em]">Projet Maven complet disponible pour consultation</p>
  </footer>

</div>