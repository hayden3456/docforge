<script>
  import LottiePlayer from '$lib/components/LottiePlayer.svelte';
  import programmerAnimation from '$lib/assets/programmer.json';
</script>

    <!-- About Us Section -->
    <section id="about-us" class="bg-amber-50 py-12 sm:py-16 md:py-20">
        <div class="container mx-auto px-4 sm:px-6">
          <div class="mx-auto max-w-7xl">
            <div class="grid gap-8 sm:gap-12 md:gap-16 lg:grid-cols-2 lg:gap-20 lg:items-center">


                <!-- Right side: Programmer animation -->
              <div class="relative">
                <div class="aspect-[4/3] w-full overflow-hidden rounded-2xl">
                  <LottiePlayer 
                    animationData={programmerAnimation}
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

              <!-- Left side: About Us content -->
              <div class="space-y-4 sm:space-y-6">
                <h2 class="text-pretty text-3xl sm:text-4xl font-bold tracking-tight text-slate-900 md:text-5xl">
                  About Us
                </h2>
                <p class="text-base sm:text-lg text-slate-600">
                    We're a team of developers who have had to "fake it till you make it" for too long. 
                    Whether it's onboarding a new team or reading code you wrote years ago, understanding a codebase is hard. 
                    With more generative AI–written code in the world, true understanding is only getting harder.
                </p>
                <p class="text-base sm:text-lg text-slate-600">
                    Our mission is to allow for deeper understanding of files, how they interact, and to map how code 
                    is advancing initiatives of the business. To become a platform for the broadest view of your business, we have to start from the foundation:
                    the internal code documentation.
                </p>
                <div class="pt-4">
                  <div class="flex items-center space-x-4">
                    <img 
                      src="/hayden_bio_cropped.jpg" 
                      alt="Hayden Constas" 
                      class="h-12 w-12 rounded-full object-cover"
                    />
                    <div>
                      <h3 class="font-semibold text-slate-900">Hayden Constas</h3>
                      <p class="text-sm text-slate-600">Founder of DocFlow</p>
                    </div>
                  </div>
                </div>
              </div>
              
              
            </div>
          </div>
        </div>
      </section>