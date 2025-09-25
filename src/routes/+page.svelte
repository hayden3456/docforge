<script>
  import Header from '$lib/components/Header.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import ProblemCard from '$lib/components/ProblemCard.svelte';
  import FeatureCard from '$lib/components/FeatureCard.svelte';
  import AboutUs from '$lib/components/aboutus.svelte';
  import StepCard from '$lib/components/StepCard.svelte';
  import Footer from '$lib/components/Footer.svelte';
  import LottiePlayer from '$lib/components/LottiePlayer.svelte';
  import autoEditAnimation from '$lib/assets/auto_edit.json';
  import programmerAnimation from '$lib/assets/programmer.json';

  // Get current year for footer
  const currentYear = new Date().getFullYear();
</script>

  <div class="min-h-screen overflow-x-hidden bg-amber-50 text-slate-800 antialiased font-sans dark:bg-slate-950 dark:text-slate-100">
    <!-- Header -->
  <Header />

    <!-- Hero -->
  <Hero />
  <AboutUs />

    <!-- Problem Section -->
    <section class="bg-amber-50 py-16 dark:bg-slate-900">
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
      </div>
    </section>

    <!-- Features / What We Do -->
    <section id="features" class="py-20">
      <div class="container mx-auto px-6">
        <div class="mx-auto max-w-2xl text-center">
          <h2 class="text-pretty text-5xl font-bold tracking-tight text-slate-900 md:text-5xl dark:text-white">Features</h2>
          <p class="mt-4 text-slate-600 dark:text-slate-300 text-2xl">Working with devs ensures docs stay relevant, knowledge transfer happens, and everyone saves time.</p>
        </div>
        
        <!-- Features Layout: Left content, Right image -->
        <div class="mx-auto mt-16 max-w-7xl">
          <div class="grid gap-16 lg:grid-cols-2 lg:gap-20 lg:items-center">
            <!-- Left side: Stacked feature cards -->
            <div class="space-y-8">
              <FeatureCard
                title="AI Documentation Generation"
                description="Generate wiki docs for legacy code directly from your codebase and commit history."
                iconBgColor="bg-brand-600/15"
                iconTextColor="text-brand-600"
                iconRingColor="ring-brand-600/20"
                gradientStyle="background:radial-gradient(600px at 0% 0%, #104C35, transparent 60%);"
                isCompact={true}
                showIcon={false}
              />
              <FeatureCard
                title="Auto-Sync with Code"
                description="Hooks into your CI to update docs on every PR merge. Changes are reviewed with diffs so your team stays in control."
                iconBgColor="bg-brand-500/15"
                iconTextColor="text-brand-500"
                iconRingColor="ring-brand-500/20"
                gradientStyle="background:radial-gradient(600px at 100% 0%, #104C35, transparent 60%);"
                isCompact={true}
                showIcon={false}
              />
            </div>
            
            <!-- Right side: Large Lottie animation window -->
            <div class="relative">
              <div class="aspect-[4/3] w-full overflow-hidden rounded-2xl">
                <LottiePlayer 
                  animationData={autoEditAnimation}
                  autoplay={true}
                  loop={true}
                  speed={1}
                  className="h-full w-full"
                />
              </div>
              <!-- Decorative elements -->
              <div class="absolute -right-4 -top-4 h-24 w-24 rounded-full bg-brand-500/10 blur-xl"></div>
              <div class="absolute -bottom-6 -left-6 h-32 w-32 rounded-full bg-brand-600/10 blur-2xl"></div>
            </div>
          </div>
        </div>
        
        <!-- Coming Soon: Dependency Mapping -->
        <div class="mx-auto mt-20 max-w-7xl">
          <div class="grid gap-16 lg:grid-cols-2 lg:gap-20 lg:items-center">
        
            <!-- Right side: Diagram -->
            <div class="relative">
              <div class="rounded-2xl p-6">
                <img src="/src/lib/assets/digram.svg" alt="Codebase dependency mapping diagram" class="w-full h-auto" />
              </div>
              <!-- Decorative elements -->
              <div class="absolute -right-4 -top-4 h-24 w-24 rounded-full bg-brand-500/10 blur-xl"></div>
              <div class="absolute -bottom-6 -left-6 h-32 w-32 rounded-full bg-brand-600/10 blur-2xl"></div>
            </div>

               <!-- Left side: Text content -->
               <div class="space-y-6">
                <h3 class="text-3xl font-bold text-slate-900 dark:text-white">Dependency Mapping (In The Works)</h3>
                <p class="text-xl text-slate-600 dark:text-slate-300">We're building functionality to automatically map dependencies and better visualize codebase integrations</p>
              </div>
              
          </div>
        </div>
      </div>
      
    </section>


    <!-- How it works -->
    <section id="how-it-works" class="bg-amber-50 py-20 dark:bg-slate-900">
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

    <!-- Security & Privacy Section -->
    <section class="">
      <div class="container mx-auto px-6">
        <div class="mx-auto max-w-4xl text-center">
          <h2 class="text-3xl font-bold text-slate-900 dark:text-white mb-8">
            No, we don't store your code
          </h2>
          <p class="text-lg text-slate-600 dark:text-slate-300 mb-8">
            Your code lives entirely in your repos. No code or documentation is ever saved on DocFlow's servers, nor is any code modified by DocFlow. We take privacy very seriously and will work with your security team in complete transparency to meet your standards.
          </p>
          <div class="flex flex-col items-center gap-6 md:flex-row md:justify-center">
            <div class="rounded-lg border border-slate-200 bg-slate-50 p-6 dark:border-slate-700 dark:bg-slate-900">
              <div class="text-center">
                <div class="mx-auto mb-3 flex h-16 w-16 items-center justify-center rounded-full bg-slate-100 dark:bg-slate-800">
                  <svg class="h-8 w-8 text-slate-600 dark:text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />
                  </svg>
                </div>
                <h3 class="font-semibold text-slate-900 dark:text-white">Security First</h3>
                <p class="text-sm text-slate-600 dark:text-slate-300">Code never leaves your environment</p>
              </div>
            </div>
            <div class="rounded-lg border border-slate-200 bg-slate-50 p-6 dark:border-slate-700 dark:bg-slate-900">
              <div class="text-center">
                <div class="mx-auto mb-3 flex h-16 w-16 items-center justify-center rounded-full bg-slate-100 dark:bg-slate-800">
                  <svg class="h-8 w-8 text-slate-600 dark:text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                </div>
                <h3 class="font-semibold text-slate-900 dark:text-white">Transparent Process</h3>
                <p class="text-sm text-slate-600 dark:text-slate-300">Work with your security team</p>
              </div>
            </div>
            <div class="rounded-lg border border-slate-200 bg-slate-50 p-6 dark:border-slate-700 dark:bg-slate-900">
              <div class="text-center">
                <div class="mx-auto mb-3 flex h-16 w-16 items-center justify-center rounded-full bg-slate-100 dark:bg-slate-800">
                  <svg class="h-8 w-8 text-slate-600 dark:text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                </div>
                <h3 class="font-semibold text-slate-900 dark:text-white">Growing Standards</h3>
                <p class="text-sm text-slate-600 dark:text-slate-300">Building toward enterprise compliance</p>
              </div>
            </div>
          </div>
          <div class="mt-8">
            <p class="text-sm text-slate-500 dark:text-slate-400">
              While we're a growing company without formal certifications yet, we're committed to meeting your security requirements through open collaboration and transparency.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
  <Footer {currentYear} />
  </div>
