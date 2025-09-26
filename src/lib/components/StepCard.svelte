<script>
  export let stepNumber = 1;
  export let title = "";
  export let description = "";
</script>

<li class="rounded-xl border border-slate-200/70 bg-white p-6 shadow-sm">
  <div class="mb-3 inline-flex h-8 w-8 items-center justify-center rounded-full bg-brand-600/15 text-sm font-bold text-brand-600 ring-1 ring-inset ring-brand-600/20">{stepNumber}</div>
  <h3 class="text-base font-semibold text-slate-900">{title}</h3>
  <p class="mt-2 text-sm text-slate-600">{description}</p>
</li>
