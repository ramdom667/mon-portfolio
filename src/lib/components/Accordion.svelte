<script>
  import { slide } from 'svelte/transition';
  export let title = "";
  let isOpen = false;
</script>

<div class="border-b border-gray-200 dark:border-gray-800">
  <button
    on:click={() => isOpen = !isOpen}
    class="w-full flex justify-between items-center py-4 text-left focus:outline-none"
  >
    <span class="text-lg font-medium">{title}</span>

    <svg
      xmlns="http://www.w3.org/2000/svg"
      fill="none"
      viewBox="0 0 24 24"
      stroke-width="2"
      stroke="currentColor"
      class="w-5 h-5 transition-transform duration-200 {isOpen ? 'rotate-180' : ''}"
    >
      <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 8.25l-7.5 7.5-7.5-7.5" />
    </svg>
  </button>

  {#if isOpen}
    <div transition:slide={{ duration: 200 }} class="pb-4 text-gray-700 dark:text-gray-300">
      <slot />
    </div>
  {/if}
</div>