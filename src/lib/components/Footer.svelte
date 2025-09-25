<script>
  export let currentYear = new Date().getFullYear();
  import whiteCrab from '../assets/white_crab.png';
</script>

<footer class="py-10 text-sm text-slate-600 dark:text-slate-400">
  <div class="container mx-auto flex flex-col items-center justify-between gap-4 px-6 md:flex-row">
    <a href="#top" class="flex items-center gap-2 text-slate-800 hover:text-slate-900 dark:text-slate-200 dark:hover:text-white">
      <span class="relative inline-flex h-12 w-12 items-center justify-center rounded-lg bg-brand-600 text-white shadow-glow">
        <img src={whiteCrab} alt="DocFlow Logo" class="h-8 w-8" />
      </span>
      <span class="font-semibold">DocFlow</span>
    </a>
    <nav class="flex items-center gap-6">
      <a href="#about-us" class="hover:text-slate-900 dark:hover:text-white">About Us</a>
      <a href="#features" class="hover:text-slate-900 dark:hover:text-white">Features</a>
      <a href="/pricing" class="hover:text-slate-900 dark:hover:text-white">Pricing</a>
    </nav>
    <p class="text-center md:text-right">© {currentYear} DocFlow. All rights reserved.</p>
  </div>
</footer>
