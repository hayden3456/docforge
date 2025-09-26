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
  import crabSvg from '$lib/assets/crab.svg';
  import network from '$lib/assets/network.svg';


  // Get current year for footer
  const currentYear = new Date().getFullYear();
</script>

  <div class="min-h-screen overflow-x-hidden bg-amber-50 text-slate-800 antialiased font-sans">
    <!-- Header -->
  <Header />

    <!-- Hero -->
  <Hero />

  <!-- Masked SVG Section -->
<section class="py-8">
  <div class="container ">
    <!-- Mobile Layout: Stacked -->
    <div class="flex flex-col lg:hidden gap-8">
      <!-- Mobile: Just show network SVG -->
      <div class="w-full h-[300px] sm:h-[400px]">
        <div class="w-full h-full flex items-center justify-center">
          <img src={network} alt="Network diagram" class="w-full h-full object-contain"/>
        </div>
      </div>
      
      <!-- Mobile: Text content -->
      <div class="w-full">
        <h2 class="text-4xl font-bold text-slate-900 mb-6">
          Understand Your Codebase Like Never Before
        </h2>
        <p class="text-lg text-slate-600 mb-4">
          Docforge gives insights to new hires working on a new function and to architects looking at integrations. With deeper understanding, there are fewer rollbacks, more time saved, and actionable planning.
        </p>
        <p class="text-lg text-slate-600 mb-6">
          We allow ICs and Managers to be on the same page. With greater understanding, everyone has less confusion and more action.
        </p>

      </div>
    </div>

    <!-- Desktop Layout: Side by side -->
    <div class="hidden lg:flex items-center gap-8">
      <!-- Desktop: Show masked SVG -->
      <div class="flex-1 max-w-4xl">
        <svg class="w-full h-auto max-h-[1200px]" viewBox="0 0 1024 1024" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid meet">
          <defs>
            <mask id="crabMask">
              <rect width="1024" height="1024" fill="black"/>
              <g transform="translate(0, 0) scale(1)">
                <path fill="white" d="M461.60 404.40 Q462.51 401.78 463.51 399.00 C466.79 389.93 459.70 378.67 452.34 374.53 C434.80 364.67 416.87 378.25 418.69 397.34 Q419.31 403.77 422.05 408.87 A0.65 0.64 -16.4 0 1 421.53 409.82 Q411.86 410.56 401.00 412.50 Q396.86 413.24 394.15 415.41 Q356.25 445.76 324.60 470.29 C321.42 472.76 319.79 474.57 316.43 471.66 Q283.19 442.85 269.37 431.21 A2.19 2.16 14.1 0 1 268.66 430.04 L259.07 388.42 A0.63 0.61 -15.8 0 1 259.49 387.69 Q299.25 374.81 309.86 371.36 Q316.18 369.30 320.90 364.41 Q372.06 311.38 388.93 294.17 Q390.95 292.11 391.67 288.41 Q399.38 248.44 405.86 213.32 C406.11 211.94 406.17 210.02 404.97 208.88 C403.21 207.19 400.03 204.97 397.57 206.11 Q396.53 206.59 395.19 207.94 Q378.33 224.94 347.37 256.37 Q344.05 259.74 341.12 261.36 Q327.22 269.03 311.05 277.43 A0.29 0.28 -7.7 0 1 310.64 277.12 Q319.01 239.23 320.66 231.68 C321.49 227.88 325.24 224.37 328.16 221.40 Q361.19 187.80 395.49 151.74 C398.54 148.53 394.00 140.23 390.24 140.93 Q351.39 148.19 316.65 154.06 Q311.95 154.86 308.66 156.07 Q302.18 158.46 301.07 159.31 Q266.68 185.51 236.59 207.96 C227.21 214.95 220.63 220.46 212.61 226.65 C209.15 229.32 206.65 232.73 205.21 236.68 Q197.33 258.15 175.05 320.06 Q173.42 324.58 172.97 328.99 Q172.57 332.86 175.32 336.39 Q196.13 363.03 204.83 373.41 Q207.34 376.40 210.43 378.91 A0.49 0.48 -35.7 0 1 210.29 379.74 C207.49 380.79 202.99 381.50 200.77 383.17 C198.56 384.82 192.16 390.50 192.76 393.32 Q199.81 426.21 204.06 446.69 Q204.78 450.14 206.18 459.38 A3.75 3.61 -66.9 0 0 206.75 460.88 C208.98 464.28 210.24 468.08 213.45 470.88 C215.64 472.80 219.53 475.04 221.55 476.17 Q223.61 477.34 273.51 509.53 Q278.44 512.71 280.53 514.22 A3.75 3.69 8.3 0 1 281.87 515.99 L300.31 567.48 A0.36 0.36 0.0 0 1 299.86 567.95 L187.54 534.77 A1.20 1.18 45.4 0 0 186.88 534.76 L179.57 536.82 A2.10 2.08 10.5 0 0 178.48 537.56 L128.60 604.22 A2.75 2.62 -20.8 0 0 128.15 605.16 Q127.64 607.17 127.42 609.23 Q123.98 641.25 119.17 680.25 C118.74 683.68 118.67 686.81 122.74 687.76 Q127.82 688.94 129.85 684.62 Q131.04 682.10 156.68 623.18 Q157.38 621.57 159.08 620.32 Q178.22 606.26 195.60 592.81 A3.21 3.19 32.1 0 1 198.22 592.22 Q257.84 605.03 321.32 620.19 A3.48 3.45 79.4 0 1 323.39 621.62 L333.58 636.52 A0.30 0.30 0.0 0 1 333.36 636.99 Q297.13 639.81 223.13 645.88 C217.50 646.34 211.05 653.11 208.52 657.25 Q190.53 686.73 172.16 715.92 Q171.18 717.47 166.70 724.95 Q165.76 726.52 165.25 731.58 A4.42 4.39 39.8 0 0 165.41 733.29 Q167.11 738.91 167.68 741.31 Q170.37 752.66 181.05 800.96 Q182.14 805.86 182.56 806.48 C185.10 810.17 190.89 807.27 192.98 804.40 A2.20 2.20 0.0 0 0 193.40 803.17 Q194.45 775.20 196.28 743.79 C196.39 741.92 196.44 740.39 197.74 738.98 Q218.37 716.68 235.98 696.69 Q239.01 693.26 244.49 692.22 Q294.97 682.67 355.81 671.44 A2.21 2.21 0.0 0 1 357.77 672.05 L363.73 678.01 A0.68 0.67 -38.2 0 1 363.60 679.07 L268.16 735.56 A1.29 1.29 0.0 0 0 267.70 736.02 Q266.33 738.28 265.38 741.12 Q256.66 767.16 246.16 800.44 Q244.25 806.49 243.12 811.41 A3.97 3.95 41.6 0 0 243.26 813.71 C245.10 818.75 245.37 820.98 248.63 824.37 C268.76 845.28 287.93 864.69 306.74 885.15 C310.26 888.98 312.26 891.68 316.99 889.17 Q321.82 886.61 319.11 881.10 Q310.43 863.49 288.87 820.83 Q288.25 819.60 287.67 817.87 A1.75 1.72 -42.3 0 1 287.74 816.59 Q299.07 791.91 307.91 772.15 C309.27 769.12 310.71 768.16 313.36 766.35 Q352.71 739.55 392.54 711.60 A1.04 1.03 -43.4 0 1 393.77 711.63 Q422.57 733.66 422.75 733.80 C427.98 737.75 430.14 739.98 436.00 739.97 Q483.22 739.90 583.50 739.97 Q589.49 739.98 590.96 739.49 C593.81 738.56 598.11 734.83 600.72 732.92 Q612.13 724.56 629.60 711.22 A1.20 1.20 0.0 0 1 631.00 711.19 Q670.20 738.46 712.91 767.58 Q715.41 769.29 715.98 770.54 Q727.91 796.73 736.90 815.92 A3.55 3.54 -44.2 0 1 736.85 819.04 Q720.92 850.48 706.69 879.37 C705.54 881.70 704.42 883.82 705.26 886.26 C706.47 889.81 712.25 891.52 714.88 888.62 Q744.91 855.42 776.86 822.60 C778.37 821.05 781.54 813.54 780.76 811.00 Q773.78 788.03 757.94 740.03 Q756.58 735.91 752.77 733.72 Q728.54 719.74 659.53 678.93 A0.62 0.62 0.0 0 1 659.40 677.96 L665.89 671.47 A1.35 1.34 27.6 0 1 667.09 671.10 C708.34 678.69 742.70 684.58 783.53 693.18 A4.64 4.58 -19.8 0 1 785.47 694.08 Q787.89 695.98 790.05 698.46 Q803.76 714.20 825.17 737.47 Q827.68 740.21 827.75 741.53 Q830.46 791.92 830.95 802.76 C831.14 806.96 836.90 808.86 840.18 807.81 A3.07 3.07 0.0 0 0 842.21 805.59 L859.19 731.84 A0.82 0.44 -54.9 0 0 859.21 731.67 C859.09 726.41 856.40 723.05 853.37 718.12 Q821.33 665.96 816.75 658.26 C813.91 653.50 809.67 649.75 805.15 647.12 Q803.35 646.07 799.25 645.75 Q741.81 641.39 690.03 637.13 A0.40 0.40 0.0 0 1 689.73 636.51 L699.69 621.43 A3.24 3.20 -79.5 0 1 701.64 620.07 Q734.47 612.21 787.02 600.32 Q811.88 594.70 824.03 592.35 Q826.95 591.79 829.03 593.45 Q846.32 607.29 865.47 621.61 A6.98 6.88 7.0 0 1 867.67 624.38 Q878.07 648.40 893.69 684.79 Q895.24 688.40 899.32 687.95 C904.88 687.32 905.14 684.46 904.55 679.50 Q899.41 635.80 896.18 606.53 A4.66 4.66 0.0 0 0 895.29 604.27 L845.51 538.16 A3.76 3.72 -7.4 0 0 843.90 536.93 Q841.34 535.90 838.01 535.07 Q836.15 534.60 832.83 535.59 Q736.80 564.14 723.26 568.17 A0.45 0.45 0.0 0 1 722.72 567.56 C728.97 553.26 732.59 541.91 741.25 517.03 Q742.09 514.61 743.49 513.72 Q759.97 503.15 809.06 472.37 Q812.05 470.50 813.10 468.33 Q815.30 463.82 817.23 460.87 A3.59 3.58 64.7 0 0 817.80 459.27 Q818.08 456.68 818.42 454.94 Q825.20 420.87 830.64 394.28 Q831.02 392.40 830.66 391.70 C828.63 387.77 824.16 383.00 819.73 381.75 Q819.61 381.72 813.81 379.81 A0.55 0.55 0.0 0 1 813.60 378.90 Q820.48 372.14 826.97 363.98 Q834.54 354.48 848.32 336.74 C850.49 333.95 850.93 332.23 850.75 328.99 Q850.53 324.85 848.90 320.37 Q821.44 244.75 818.54 236.68 C817.41 233.55 815.58 229.86 813.53 228.23 Q798.41 216.21 795.21 213.79 Q749.59 179.26 727.02 162.01 Q721.98 158.16 718.48 156.83 Q713.75 155.03 708.77 154.20 Q666.28 147.09 634.33 141.00 C631.02 140.37 628.80 143.80 627.70 146.50 Q626.37 149.78 628.77 152.24 Q661.96 186.36 700.68 225.82 Q703.50 228.69 703.84 230.22 Q709.38 254.77 714.17 277.41 A0.29 0.29 0.0 0 1 713.75 277.73 Q700.46 270.83 689.04 264.74 C684.66 262.41 681.06 260.48 677.78 257.14 Q664.71 243.85 628.19 207.06 C625.51 204.36 622.65 206.20 619.94 208.23 C618.28 209.46 617.80 211.35 618.19 213.27 Q625.27 247.95 632.72 288.40 Q633.36 291.86 635.30 293.90 Q654.62 314.18 699.45 360.09 C704.73 365.49 707.50 368.64 712.68 370.36 Q736.94 378.38 764.81 387.74 A0.39 0.39 0.0 0 1 765.07 388.20 L755.41 430.15 A2.90 2.86 -12.7 0 1 754.37 431.77 Q750.74 434.55 747.68 437.18 Q727.48 454.62 707.43 472.17 Q705.25 474.09 703.06 472.41 Q674.68 450.77 631.49 416.52 Q626.40 412.49 619.29 411.42 Q612.61 410.42 602.24 409.45 A0.46 0.46 0.0 0 1 601.87 408.79 Q607.70 396.79 603.42 385.84 C597.41 370.48 579.67 366.74 567.56 377.69 Q562.05 382.66 559.66 390.30 C558.12 395.23 559.91 399.75 561.86 404.02 A0.49 0.49 0.0 0 1 561.42 404.71 L461.81 404.71 A0.23 0.23 0.0 0 1 461.60 404.40"/>
              </g>
            </mask>
          </defs>
          
          <!-- Background -->
          <rect width="1024" height="1024" fill="#104C35" mask="url(#crabMask)"/>
          
          <!-- Test SVG content as foreign object -->
          <foreignObject x="200" y="450" width="700" height="400" mask="url(#crabMask)">
            <div xmlns="http://www.w3.org/1999/xhtml" class="w-full h-full">
              <img src={network} alt="Masked SVG content" class="w-full h-full object-contain"/>
            </div>
          </foreignObject>
        </svg>
      </div>
      
      <!-- Desktop: Text content -->
      <div class="flex-1 max-w-lg">
        <h2 class="text-3xl xl:text-4xl font-bold text-slate-900 mb-6">
          Understand Your Codebase Like Never Before
        </h2>
        <p class="text-lg xl:text-2xl text-slate-600 mb-4">
          Docforge gives insights to new hires working on a new function and to architects looking at integrations. With deeper understanding, there are fewer rollbacks, more time saved, and actionable planning.
        </p>
        <p class="text-lg xl:text-2xl text-slate-600 mb-6">
          We allow ICs and Managers to be on the same page. With greater understanding, everyone has less confusion and more action.
        </p>
      </div>
    </div>
  </div>
</section>

  
    <!-- Problem Section -->
    <section class="bg-amber-50 py-12 sm:py-16">
      <div class="container mx-auto px-4 sm:px-6">
        <h2 class="text-pretty text-center text-2xl sm:text-3xl font-bold tracking-tight text-slate-900 md:text-4xl">
          Documentation Is Broken 
        </h2>
      <div class="mx-auto mt-10 grid max-w-8xl gap-4 sm:gap-6 grid-cols-1 md:grid-cols-3 items-stretch">
        <ProblemCard
          hasCodeExample={true}
          title="Docs out of sync"
          description="Documentation becomes outdated the moment code changes, leaving developers confused and frustrated."
        />
        <ProblemCard
          hasCodeExample={true}
          title="Tribal Knowledge Leaves"
          description="Critical knowledge walks out the door with departing team members, creating knowledge gaps."
          imageSrc="/walking.png"
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
    <section id="features" class="py-12 sm:py-16 md:py-20">
      <div class="container mx-auto px-4 sm:px-6">
        <div class="mx-auto max-w-2xl text-center">
          <h2 class="text-pretty text-3xl sm:text-4xl md:text-5xl font-bold tracking-tight text-slate-900">Features</h2>
          <p class="mt-4 text-slate-600 text-lg sm:text-xl md:text-2xl">Working with devs ensures docs stay relevant, knowledge transfer happens, and everyone saves time.</p>
        </div>
        
        <!-- Features Layout: Left content, Right image -->
        <div class="mx-auto mt-8 sm:mt-12 md:mt-16 max-w-7xl">
          <div class="grid gap-8 sm:gap-12 md:gap-16 lg:grid-cols-2 lg:gap-20 lg:items-center">
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
        <div class="mx-auto mt-12 sm:mt-16 md:mt-20 max-w-7xl">
          <div class="grid gap-8 sm:gap-12 md:gap-16 lg:grid-cols-2 lg:gap-20 lg:items-center">
        
            <!-- Right side: Diagram -->
            <div class="relative">
              <div class="rounded-2xl p-6">
                <img src="/digram.svg" alt="Codebase dependency mapping diagram" class="w-full h-auto" />
              </div>
              <!-- Decorative elements -->
              <div class="absolute -right-4 -top-4 h-24 w-24 rounded-full bg-brand-500/10 blur-xl"></div>
              <div class="absolute -bottom-6 -left-6 h-32 w-32 rounded-full bg-brand-600/10 blur-2xl"></div>
            </div>

               <!-- Left side: Text content -->
               <div class="space-y-4 sm:space-y-6">
                <h3 class="text-2xl sm:text-3xl font-bold text-slate-900">Dependency Mapping (In The Works)</h3>
                <p class="text-lg sm:text-xl text-slate-600">We're building functionality to automatically map dependencies and better visualize codebase integrations</p>
              </div>
              
          </div>
        </div>
      </div>
      
    </section>


    <!-- How it works -->
    <section id="how-it-works" class="bg-amber-50 py-12 sm:py-16 md:py-20">
      <div class="container mx-auto px-4 sm:px-6">
        <div class="mx-auto max-w-2xl text-center">
          <h2 class="text-pretty text-2xl sm:text-3xl font-bold tracking-tight text-slate-900 md:text-4xl">How It Works</h2>
          <p class="mt-4 text-slate-600 text-lg sm:text-xl">Zero-friction setup. Real documentation value from day one.</p>
        </div>
        <ol class="mx-auto mt-8 sm:mt-12 grid max-w-7xl gap-4 sm:gap-6 grid-cols-1 sm:grid-cols-2 md:grid-cols-3">
        <StepCard
          stepNumber={1}
          title="Connect your repo"
          description="Point StrideDocs at GitHub, GitLab, or Bitbucket. We index your code and existing docs."
        />
        <StepCard
          stepNumber={2}
          title="Generate & review"
          description="We propose doc changes with clear diffs. Your team accepts, edits, or declines. Always in control."
        />
        <StepCard
          stepNumber={3}
          title="Stay in sync"
          description="On every merge, docs update automatically. Knowledge sticks even when people move on. If you don't like us, take your markdown docs and run. It's yours."
        />
        </ol>
      </div>
    </section>

    <!-- Security & Privacy Section -->
    <section class="py-12 sm:py-16 md:py-20">
      <div class="container mx-auto px-4 sm:px-6">
        <div class="mx-auto max-w-4xl text-center">
          <h2 class="text-2xl sm:text-3xl font-bold text-slate-900 mb-6 sm:mb-8">
            No, we don't store your code
          </h2>
          <p class="text-base sm:text-lg text-slate-600 mb-6 sm:mb-8">
            Your code lives entirely in your repos. No code or documentation is ever saved on DocFlow's servers, nor is any code modified by DocFlow. We take privacy very seriously and will work with your security team in complete transparency to meet your standards.
          </p>
          <div class="flex flex-col items-center gap-4 sm:gap-6 md:flex-row md:justify-center">
            <div class="rounded-lg border border-slate-200 bg-slate-50 p-4 sm:p-6 w-full md:w-auto">
              <div class="text-center">
                <div class="mx-auto mb-3 flex h-16 w-16 items-center justify-center rounded-full bg-slate-100 ">
                  <svg class="h-8 w-8 text-slate-600 " fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />
                  </svg>
                </div>
                <h3 class="font-semibold text-slate-900 ">Security First</h3>
                <p class="text-sm text-slate-600 ">Code never leaves your environment</p>
              </div>
            </div>
            <div class="rounded-lg border border-slate-200 bg-slate-50 p-4 sm:p-6 w-full md:w-auto">
              <div class="text-center">
                <div class="mx-auto mb-3 flex h-16 w-16 items-center justify-center rounded-full bg-slate-100 ">
                  <svg class="h-8 w-8 text-slate-600 " fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                </div>
                <h3 class="font-semibold text-slate-900 ">Transparent Process</h3>
                <p class="text-sm text-slate-600 ">Work with your security team</p>
              </div>
            </div>
            <div class="rounded-lg border border-slate-200 bg-slate-50 p-4 sm:p-6 w-full md:w-auto">
              <div class="text-center">
                <div class="mx-auto mb-3 flex h-16 w-16 items-center justify-center rounded-full bg-slate-100 ">
                  <svg class="h-8 w-8 text-slate-600 " fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                </div>
                <h3 class="font-semibold text-slate-900 ">Growing Standards</h3>
                <p class="text-sm text-slate-600 ">Building toward enterprise compliance</p>
              </div>
            </div>
          </div>
          <div class="mt-6 sm:mt-8">
            <p class="text-xs sm:text-sm text-slate-500">
              While we're a growing company without formal certifications yet, we're committed to meeting your security requirements through open collaboration and transparency.
            </p>
          </div>
        </div>
      </div>
    </section>

    <AboutUs />


    <!-- Footer -->
  <Footer {currentYear} />
  </div>
