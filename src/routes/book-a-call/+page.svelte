<script>
  import Header from '$lib/components/Header.svelte';
  import Footer from '$lib/components/Footer.svelte';
  import { onMount } from 'svelte';
  
  // Get current year for footer
  const currentYear = new Date().getFullYear();

  onMount(() => {
    // Load Calendly script dynamically
    const script = document.createElement('script');
    script.type = 'text/javascript';
    script.src = 'https://assets.calendly.com/assets/external/widget.js';
    script.async = true;
    document.head.appendChild(script);
  });
</script>

<div class="min-h-screen overflow-x-hidden bg-amber-50 text-slate-800 antialiased font-sans dark:bg-slate-950 dark:text-slate-100">
  <!-- Header -->
  <Header />

  <!-- Booking Hero -->
  <section class="py-16">
    <div class="container mx-auto px-6">
      <div class="mx-auto max-w-4xl text-center">
        <h1 class="text-pretty text-4xl font-bold tracking-tight text-slate-900 md:text-5xl dark:text-white">
          Book a Call
        </h1>
        <p class="mt-6 text-xl text-slate-600 dark:text-slate-300">
          Let's discuss how DocFlow can help your organization with documentation automation and custom features.
        </p>
        <div class="mt-8 rounded-lg bg-white p-6 shadow-sm dark:bg-slate-800">
          <div class="grid gap-4 md:grid-cols-3">
            <div class="text-center">
              <div class="mx-auto mb-2 flex h-12 w-12 items-center justify-center rounded-full bg-brand-100 dark:bg-brand-900/20">
                <svg class="h-6 w-6 text-brand-600 dark:text-brand-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
              </div>
              <h3 class="font-semibold text-slate-900 dark:text-white">30 Minutes</h3>
              <p class="text-sm text-slate-600 dark:text-slate-300">Quick consultation</p>
            </div>
            <div class="text-center">
              <div class="mx-auto mb-2 flex h-12 w-12 items-center justify-center rounded-full bg-brand-100 dark:bg-brand-900/20">
                <svg class="h-6 w-6 text-brand-600 dark:text-brand-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
              </div>
              <h3 class="font-semibold text-slate-900 dark:text-white">No Commitment</h3>
              <p class="text-sm text-slate-600 dark:text-slate-300">Free consultation</p>
            </div>
            <div class="text-center">
              <div class="mx-auto mb-2 flex h-12 w-12 items-center justify-center rounded-full bg-brand-100 dark:bg-brand-900/20">
                <svg class="h-6 w-6 text-brand-600 dark:text-brand-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                </svg>
              </div>
              <h3 class="font-semibold text-slate-900 dark:text-white">Quick Setup</h3>
              <p class="text-sm text-slate-600 dark:text-slate-300">Free assistance</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Calendly Widget -->
  <section class="pb-20">
    <div class="container mx-auto px-6">
      <div class="mx-auto max-w-4xl">
        <div class="rounded-2xl bg-white p-8 shadow-lg dark:bg-slate-800">
          <div class="mb-6 text-center">
            <h2 class="text-2xl font-bold text-slate-900 dark:text-white">Schedule Your Call</h2>
            <p class="mt-2 text-slate-600 dark:text-slate-300">
              Choose a time that works for you. We'll discuss your documentation needs and how DocFlow can help.
            </p>
          </div>
          
          <!-- Calendly Widget -->
          <div class="calendly-inline-widget" 
               data-url="https://calendly.com/haydenconstas/meeting?hide_event_type_details=1" 
               style="min-width:320px;height:700px;">
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- What to Expect Section -->
  <section class="bg-amber-50 py-16 dark:bg-slate-900">
    <div class="container mx-auto px-6">
      <div class="mx-auto max-w-4xl">
        <h2 class="text-center text-3xl font-bold text-slate-900 dark:text-white">What to Expect</h2>
        <div class="mt-12 grid gap-8 md:grid-cols-2">
          <div class="rounded-lg bg-white p-6 shadow-sm dark:bg-slate-800">
            <h3 class="text-xl font-semibold text-slate-900 dark:text-white">During the Call</h3>
            <ul class="mt-4 space-y-3 text-slate-600 dark:text-slate-300">
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span>Review your current documentation challenges</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span>Demo DocFlow's capabilities</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span>Discuss custom features for your org</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span>Answer any questions you have</span>
              </li>
            </ul>
          </div>
          
          <div class="rounded-lg bg-white p-6 shadow-sm dark:bg-slate-800">
            <h3 class="text-xl font-semibold text-slate-900 dark:text-white">After the Call</h3>
            <ul class="mt-4 space-y-3 text-slate-600 dark:text-slate-300">
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span>Follow-up with detailed proposal</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span>Free setup assistance if you decide to proceed</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span>No pressure, no obligation</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span>Ongoing support available</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <Footer {currentYear} />
</div>
