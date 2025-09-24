<script>
  export let currentYear = new Date().getFullYear();
</script>

<footer class="py-10 text-sm text-slate-600 dark:text-slate-400">
  <div class="container mx-auto flex flex-col items-center justify-between gap-4 px-6 md:flex-row">
    <a href="#top" class="flex items-center gap-2 text-slate-800 hover:text-slate-900 dark:text-slate-200 dark:hover:text-white">
      <span class="inline-flex h-6 w-6 items-center justify-center rounded-md bg-gradient-to-br from-brand-500 to-brand-700 text-white">
        <svg viewBox="0 0 24 24" class="h-3.5 w-3.5" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M4 12h16" />
          <path d="M8 8h8M8 16h8" />
        </svg>
      </span>
      <span class="font-semibold">StrideDocs</span>
    </a>
    <nav class="flex items-center gap-6">
      <a href="#how-it-works" class="hover:text-slate-900 dark:hover:text-white">How it works</a>
      <a href="#features" class="hover:text-slate-900 dark:hover:text-white">Features</a>
    </nav>
    <p class="text-center md:text-right">© {currentYear} StrideDocs. All rights reserved.</p>
  </div>
</footer>
