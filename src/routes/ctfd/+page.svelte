<script>
  import { base } from '$app/paths';

  const extensions = [
    {
      title: "Rôle Modérateur Sur-Mesure",
      lang: "Python & Flask",
      desc: "Développement d'un système de permissions intermédiaire. Le plugin intercepte les requêtes backend pour bloquer l'accès aux configurations sensibles et injecte du JavaScript pour épurer l'interface d'administration.",
      features: ["Blocage de routes API", "Injection UI conditionnelle", "Gestion d'ID spécifiques"],
      link: "https://github.com/ramdom667/ctfd-moderator-role"
    },
    {
      title: "Compteur Internationalisé",
      lang: "JavaScript",
      desc: "Développement d'un système de compte à rebours dynamique supportant plus de 20 langues. Il synchronise les données temporelles de l'API CTFd pour une précision absolue durant l'événement.",
      features: ["Support i18n (FR, EN, JA, etc.)", "Détection automatique de langue", "Formatage intelligent"],
      link: "https://github.com/ramdom667/ctfd-event-countdown"
    },
    {
      title: "Discord Monitoring Bot",
      lang: "Python (discord.py)",
      desc: "Automatisation du suivi de compétition. Le bot interroge l'API toutes les 15 secondes pour diffuser les annonces et l'ouverture des défis, tout en respectant les prérequis de déblocage.",
      features: ["Polling API asynchrone", "Notifications temps réel", "Embeds dynamiques"],
      link: "https://github.com/ramdom667/ctfd-discord-bot"
    }
  ];

  const pillars = [
    { icon: "🤝", title: "Client-Centric", desc: "Feedback continu" },
    { icon: "🏃‍♂️", title: "Agile Scrum", desc: "Sprints itératifs" },
    { logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg", title: "Docker", desc: "Conteneurisation" },
    { logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg", title: "Python", desc: "Backend & Bot" },
    { logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg", title: "JavaScript", desc: "Frontend & API" }
  ];
</script>

<div class="max-w-5xl mx-auto px-6 py-12 space-y-24">
  <header class="text-center space-y-6">
    <div class="inline-block px-3 py-1 bg-red-100 dark:bg-red-900/30 text-red-700 dark:text-red-400 rounded-full text-xs font-bold uppercase tracking-widest">
      Agile Scrum • Docker • Fullstack
    </div>
    <h1 class="text-5xl md:text-7xl font-black tracking-tighter uppercase italic">
      CTFd <span class="text-red-600">Ecosystem</span>
    </h1>
    <p class="text-xl text-gray-500 max-w-3xl mx-auto italic">
      Une infrastructure robuste alliant accessibilité inclusive et automatisation avancée.
    </p>
  </header>

  <section class="grid lg:grid-cols-2 gap-16 items-start">
    <div class="space-y-6">
      <h2 class="text-3xl font-bold italic flex items-center gap-3">
        <span class="w-1.5 h-8 bg-red-600 rounded-full"></span>
        Méthodologie & Écosystème
      </h2>
      <div class="text-gray-700 dark:text-gray-300 leading-relaxed text-lg space-y-4 italic">
        <p>
          Ce projet a été mené selon la méthode <strong>Agile Scrum</strong>, en co-conception constante avec un <strong>client précis</strong>. Cette approche itérative a permis de transformer CTFd en un écosystème global répondant à des exigences de production réelles.
        </p>
        <p>
          L'interface a été repensée pour être <strong>sobre et inclusive</strong>, prévenant les risques d'épilepsie et intégrant des modes de vision adaptés aux daltonismes <strong>Deutan et Tritan</strong>.
        </p>
        <p>
          La stack technique composée de <strong>Python, JavaScript et Docker</strong> a permis d'automatiser l'infrastructure et de développer des extensions sur-mesure pour la modération et l'expérience utilisateur.
        </p>
      </div>
    </div>
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-2 gap-4">
      {#each pillars as pillar}
        <div class="p-4 bg-gray-50 dark:bg-gray-800/50 rounded-3xl border border-gray-100 dark:border-gray-700 text-center shadow-sm transition-transform hover:scale-105">
          {#if pillar.logo}
            <img src={pillar.logo} alt={pillar.title} class="w-8 h-8 mx-auto mb-2" />
          {:else}
            <span class="block text-2xl mb-2">{pillar.icon}</span>
          {/if}
          <span class="block text-[10px] font-black uppercase tracking-widest">{pillar.title}</span>
          <p class="text-[9px] text-gray-400 mt-1 italic">{pillar.desc}</p>
        </div>
      {/each}
    </div>
  </section>

  <section class="space-y-12">
    <div class="text-center">
      <h2 class="text-3xl font-bold italic uppercase tracking-tighter underline decoration-red-600 underline-offset-8 decoration-4">Modules Spécifiques</h2>
    </div>

    <div class="grid lg:grid-cols-3 gap-8">
      {#each extensions as item}
        <div class="bg-white dark:bg-gray-800/40 p-8 rounded-[2.5rem] border border-gray-100 dark:border-gray-800 flex flex-col justify-between hover:border-red-500/50 transition-all group shadow-lg">
          <div class="space-y-6">
            <div class="flex justify-between items-start">
              <h3 class="text-xl font-black italic">{item.title}</h3>
              <span class="text-[8px] font-black uppercase px-2 py-1 bg-red-50 dark:bg-red-900/20 text-red-600 rounded italic">{item.lang}</span>
            </div>
            <p class="text-gray-600 dark:text-gray-400 text-sm leading-relaxed italic">
              {item.desc}
            </p>
            <div class="flex flex-wrap gap-2">
              {#each item.features as feat}
                <span class="text-[9px] font-bold text-gray-400 uppercase tracking-widest bg-gray-100 dark:bg-gray-900 px-2 py-1 rounded-md">
                  {feat}
                </span>
              {/each}
            </div>
          </div>
          <div class="mt-8 pt-6 border-t border-gray-50 dark:border-gray-700 text-center">
            <a href={item.link} target="_blank" class="text-xs font-black uppercase tracking-widest text-red-500 flex items-center gap-2 justify-center">
              Dépôt Git <span>→</span>
            </a>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <div class="rounded-[3rem] overflow-hidden shadow-2xl bg-black border border-gray-800 relative group">
    <div class="absolute inset-0 bg-red-600/10 opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none"></div>
    <img src="{base}/ctfd-main.png" alt="CTFd Interface" class="w-full h-auto" />
  </div>
</div>