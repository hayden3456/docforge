<section id="top" class="relative isolate overflow-hidden">
  <div class="absolute inset-0 -z-10 bg-hero-gradient"></div>
  <div class="absolute inset-0 -z-10 bg-grid opacity-[0.04] [background-size:24px_24px]" style="background-image:linear-gradient(to_right,rgba(15,23,42,0.06)_1px,transparent_1px),linear-gradient(to_bottom,rgba(15,23,42,0.06)_1px,transparent_1px);"></div>
  <div class="container mx-auto grid gap-10 px-6 py-20 md:py-28 lg:grid-cols-12 lg:items-center lg:gap-12">
    <div class="relative z-10 space-y-6 lg:col-span-7">
      <p class="inline-flex items-center gap-2 rounded-full border border-slate-200/70 bg-white/80 px-3 py-1 text-xs font-medium text-slate-700 shadow-sm backdrop-blur dark:border-slate-800/60 dark:bg-slate-900/60 dark:text-slate-200">
        <span class="inline-flex h-2 w-2 rounded-full bg-brand-500"></span>
        Always in sync with your codebase
      </p>
      <h1 class="text-balance text-4xl font-extrabold tracking-tight text-slate-900 sm:text-5xl md:text-6xl dark:text-white">
        <span class="bg-gradient-to-br from-slate-900 to-slate-700 bg-clip-text text-transparent dark:from-white dark:to-slate-300">The AI Documentation Tool</span>
      </h1>
      <p class="max-w-2xl text-pretty text-lg leading-relaxed text-slate-600 md:text-xl dark:text-slate-300">
        Working with devs ensures docs stay relevant, knowledge transfer happens, and devs save time.
      </p>
      <div class="flex flex-wrap gap-3">
        <a href="#how-it-works" class="inline-flex items-center justify-center rounded-md bg-brand-600 px-5 py-3 text-sm font-semibold text-white shadow-glow transition hover:bg-brand-700 focus:outline-none focus-visible:ring-2 focus-visible:ring-brand-500/60">
          See How It Works
        </a>
        <a href="#features" class="inline-flex items-center justify-center rounded-md border border-slate-300/80 bg-white px-5 py-3 text-sm font-semibold text-slate-800 transition hover:border-slate-400 hover:bg-slate-50 dark:border-slate-700 dark:bg-slate-900 dark:text-slate-100 dark:hover:bg-slate-800">
          Explore Features
        </a>
      </div>
      <div class="flex items-center gap-6 pt-4 text-sm text-slate-500 dark:text-slate-400">
        <div class="flex items-center gap-2"><span class="h-2 w-2 rounded-full bg-brand-500"></span> Auto-updates on merge</div>
        <div class="flex items-center gap-2"><span class="h-2 w-2 rounded-full bg-brand-400"></span> IDE & CI friendly</div>
        <div class="flex items-center gap-2"><span class="h-2 w-2 rounded-full bg-brand-300"></span> Human-in-the-loop</div>
      </div>
    </div>
    <div class="relative lg:col-span-5">
      <div class="relative rounded-2xl border border-slate-200/70 bg-white/70 p-4 shadow-xl ring-1 ring-white/20 backdrop-blur-md dark:border-slate-800/70 dark:bg-slate-900/60 dark:ring-white/10">
        <div class="overflow-hidden rounded-xl bg-slate-900/95">
          <div class="flex items-center justify-between border-b border-slate-700/60 px-4 py-2 text-xs text-slate-300">
            <span class="flex items-center gap-1.5"><span class="h-2 w-2 rounded-full bg-rose-400"></span><span class="h-2 w-2 rounded-full bg-amber-400"></span><span class="h-2 w-2 rounded-full bg-emerald-400"></span></span>
            <span>doc-update.yml • CI</span>
          </div>
          <pre class="max-h-[360px] overflow-auto p-4 text-[12px]/6 text-slate-200"><code># Auto-sync documentation with code changes
on: [push]

jobs:
  generate-docs:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Analyze code changes
        run: stridedocs analyze --since $&#123;&#123; github.sha &#125;&#125;
      - name: Update docs
        run: stridedocs sync --commit
</code></pre>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
.bg-grid {
  background-size: 24px 24px;
}
</style>
