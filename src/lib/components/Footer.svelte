<script>
  export let currentYear = new Date().getFullYear();
  import whiteCrab from '../assets/white_crab.png';
</script>

<footer class="py-8 sm:py-10 text-sm text-slate-600">
  <div class="container mx-auto flex flex-col items-center justify-between gap-4 px-4 sm:px-6 md:flex-row">
    <a href="#top" class="flex items-center gap-2 text-slate-800 hover:text-slate-900">
      <span class="relative inline-flex h-10 w-10 sm:h-12 sm:w-12 items-center justify-center rounded-lg bg-brand-600 text-white shadow-glow">
        <img src={whiteCrab} alt="DocFlow Logo" class="h-6 w-6 sm:h-8 sm:w-8" />
      </span>
      <span class="font-semibold">DocFlow</span>
    </a>
    <nav class="flex items-center gap-4 sm:gap-6 text-sm">
      <a href="#about-us" class="hover:text-slate-900">About Us</a>
      <a href="#features" class="hover:text-slate-900">Features</a>
      <a href="/pricing" class="hover:text-slate-900">Pricing</a>
    </nav>
    <p class="text-center text-xs sm:text-sm md:text-right">© {currentYear} DocFlow. All rights reserved.</p>
  </div>
</footer>
