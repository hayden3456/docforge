<script>
  export let icon = "🧠";
  export let title = "";
  export let description = "";
  export let iconBgColor = "bg-brand-600/15";
  export let iconTextColor = "text-brand-600";
  export let iconRingColor = "ring-brand-600/20";
  export let gradientStyle = "background:radial-gradient(600px at 0% 0%, rgba(124,92,255,.10), transparent 60%);";
</script>

<div class="group relative rounded-2xl border border-slate-200/70 bg-white p-6 shadow-sm transition hover:shadow-md dark:border-slate-800/70 dark:bg-slate-950">
  <div class="mb-3 inline-flex h-10 w-10 items-center justify-center rounded-lg {iconBgColor} {iconTextColor} ring-1 ring-inset {iconRingColor}">{icon}</div>
  <h3 class="text-lg font-semibold text-slate-900 dark:text-slate-100">{title}</h3>
  <p class="mt-2 text-sm leading-6 text-slate-600 dark:text-slate-400">{description}</p>
  <div class="pointer-events-none absolute -inset-x-1 -inset-y-1 -z-10 rounded-3xl opacity-0 blur-2xl transition duration-500 group-hover:opacity-100" style="{gradientStyle}"></div>
</div>
