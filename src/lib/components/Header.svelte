<script>
  import whiteCrab from '../assets/white_crab.png';
</script>

<header class="sticky top-0 z-40 w-full bg-amber-50 backdrop-blur-md dark:bg-slate-950">
  <div class="container mx-auto flex h-16 items-center justify-between">
    <a href="/" class="group flex items-center gap-3 pl-2">
      <span class="relative inline-flex h-12 w-12 items-center justify-center rounded-lg bg-brand-600 text-white shadow-glow">
        <img src={whiteCrab} alt="DocFlow Logo" class="h-8 w-8" />
      </span>
      <span class="text-xl font-semibold tracking-tight text-slate-900 dark:text-white">DocFlow</span>
    </a>
    <nav class="hidden items-center gap-6 text-sm text-slate-600 md:flex dark:text-slate-300">
      <a href="#about-us" class="hover:text-slate-900 dark:hover:text-white">About Us</a>
      <a href="#features" class="hover:text-slate-900 dark:hover:text-white">Features</a>
      <a href="/pricing" class="hover:text-slate-900 dark:hover:text-white">Pricing</a>
    </nav>
    <div class="flex items-center gap-2">
      <a href="/book-a-call" class="inline-flex items-center justify-center rounded-md bg-brand-600 px-3.5 py-2 text-sm font-semibold text-white shadow-glow transition hover:bg-brand-700 focus:outline-none focus-visible:ring-2 focus-visible:ring-brand-500/60">
        Contact Us
      </a>
    </div>
  </div>
</header>
