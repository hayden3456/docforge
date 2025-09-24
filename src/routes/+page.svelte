<script>
  import Header from '$lib/components/Header.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import ProblemCard from '$lib/components/ProblemCard.svelte';
  import FeatureCard from '$lib/components/FeatureCard.svelte';
  import StepCard from '$lib/components/StepCard.svelte';
  import Footer from '$lib/components/Footer.svelte';

  // Get current year for footer
  const currentYear = new Date().getFullYear();
</script>

  <div class="min-h-screen overflow-x-hidden bg-white text-slate-800 antialiased font-sans dark:bg-slate-950 dark:text-slate-100">
    <!-- Header -->
  <Header />

    <!-- Hero -->
  <Hero />

    <!-- Problem Section -->
    <section class="bg-white py-16 dark:bg-slate-900">
      <div class="container mx-auto px-6">
        <h2 class="text-pretty text-center text-3xl font-bold tracking-tight text-slate-900 md:text-4xl dark:text-white">
          What if documentation didn't suck?
        </h2>
      <div class="mx-auto mt-10 grid max-w-8xl gap-6 md:grid-cols-3 items-stretch">
        <ProblemCard
          hasCodeExample={true}
          title="Docs out of sync"
          description="Documentation becomes outdated the moment code changes, leaving developers confused and frustrated."
        />
        <ProblemCard
          hasCodeExample={true}
          title="Tribal Knowledge Leaves"
          description="Critical knowledge walks out the door with departing team members, creating knowledge gaps."
          imageSrc="/src/lib/assets/walking.png"
        />
        <ProblemCard
          title='Getting Info Takes Too Long'
          description="It's always a longer process than it should tracking donw answers, disrupting everyone's workflow."
          hasTextBubble={true}
          bubbleText="you got a minute?"
        />
        </div>
        <p class="mx-auto mt-10 max-w-3xl text-center text-sm text-slate-600 dark:text-slate-400">It doesn't have to be this way</p>
      </div>
    </section>

    <!-- Features / What We Do -->
    <section id="features" class="py-20">
      <div class="container mx-auto px-6">
        <div class="mx-auto max-w-2xl text-center">
          <h2 class="text-pretty text-3xl font-bold tracking-tight text-slate-900 md:text-4xl dark:text-white">What We Do</h2>
          <p class="mt-4 text-slate-600 dark:text-slate-300">Purpose-built to keep docs living, accurate, and effortless.</p>
        </div>
      <div class="mx-auto mt-10 grid max-w-7xl gap-6 md:grid-cols-2">
        <FeatureCard
          icon="🧠"
          title="AI Documentation Generation"
          description="Continuously generates and refines README files, API docs, and architectural notes directly from your codebase and commit history."
          iconBgColor="bg-brand-600/15"
          iconTextColor="text-brand-600"
          iconRingColor="ring-brand-600/20"
          gradientStyle="background:radial-gradient(600px at 0% 0%, #104C35, transparent 60%);"
        />
        <FeatureCard
          icon="🔁"
          title="Auto-Sync with Code"
          description="Hooks into your CI to update docs on every PR merge. Changes are reviewed with diffs so your team stays in control."
          iconBgColor="bg-brand-500/15"
          iconTextColor="text-brand-500"
          iconRingColor="ring-brand-500/20"
          gradientStyle="background:radial-gradient(600px at 100% 0%, #104C35, transparent 60%);"
        />
      </div>
      </div>
    </section>

    <!-- How it works -->
    <section id="how-it-works" class="bg-white py-20 dark:bg-slate-900">
      <div class="container mx-auto px-6">
        <div class="mx-auto max-w-2xl text-center">
          <h2 class="text-pretty text-3xl font-bold tracking-tight text-slate-900 md:text-4xl dark:text-white">How It Works</h2>
          <p class="mt-4 text-slate-600 dark:text-slate-300">Zero-friction setup. Real documentation value from day one.</p>
        </div>
        <ol class="mx-auto mt-12 grid max-w-7xl gap-6 md:grid-cols-3">
        <StepCard
          stepNumber={1}
          title="Connect your repo"
          description="Point StrideDocs at GitHub, GitLab, or Bitbucket. We index your code and existing docs."
        />
        <StepCard
          stepNumber={2}
          title="Generate & review"
          description="We propose doc changes with clear diffs. Your team accepts, edits, or declines—always in control."
        />
        <StepCard
          stepNumber={3}
          title="Stay in sync"
          description="On every merge, docs update automatically. Knowledge sticks—even when people move on."
        />
        </ol>
      </div>
    </section>

    <!-- Footer -->
  <Footer {currentYear} />
  </div>
