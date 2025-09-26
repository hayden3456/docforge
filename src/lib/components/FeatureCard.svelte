<script>
  export let icon = "🧠";
  export let title = "";
  export let description = "";
  export let iconBgColor = "bg-brand-600/15";
  export let iconTextColor = "text-brand-600";
  export let iconRingColor = "ring-brand-600/20";
  export let gradientStyle = "background:radial-gradient(600px at 0% 0%, rgba(124,92,255,.10), transparent 60%);";
  export let isCompact = false;
  export let showIcon = true;
</script>

<div class="group relative rounded-2xls">
  <div class="flex items-start {showIcon ? 'gap-4' : ''}">
    <div class="flex-1 min-w-0">
      <h3 class="text-3xl font-extrabold text-slate-900 {isCompact ? 'text-2xl' : ''}">{title}</h3>
      <p class="mt-4 text-xl leading-9 text-slate-600 {isCompact ? 'text-lg leading-8' : ''}">{description}</p>
    </div>
  </div>
</div>
