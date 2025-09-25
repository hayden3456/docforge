<script>
  import Header from '$lib/components/Header.svelte';
  import Footer from '$lib/components/Footer.svelte';
  
  // Get current year for footer
  const currentYear = new Date().getFullYear();
</script>

<div class="min-h-screen overflow-x-hidden bg-amber-50 text-slate-800 antialiased font-sans dark:bg-slate-950 dark:text-slate-100">
  <!-- Header -->
  <Header />

  <!-- Pricing Hero -->
  <section class="py-20">
    <div class="container mx-auto px-6">
      <div class="mx-auto max-w-3xl text-center">
        <h1 class="text-pretty text-4xl font-bold tracking-tight text-slate-900 md:text-5xl dark:text-white">
          Simple, transparent pricing
        </h1>
        <p class="mt-6 text-xl text-slate-600 dark:text-slate-300">
          Choose the plan that fits your project. No hidden fees, no surprises.
        </p>
      </div>
    </div>
  </section>

  <!-- Pricing Cards -->
  <section class="pb-20">
    <div class="container mx-auto px-6">
      <div class="mx-auto grid max-w-5xl gap-8 md:grid-cols-2">
        
        <!-- Open Source Tier -->
        <div class="relative rounded-2xl border border-slate-200 bg-white p-8 shadow-sm dark:border-slate-700 dark:bg-slate-800">
          <div class="text-center">
            <h3 class="text-2xl font-bold text-slate-900 dark:text-white">Open Source</h3>
            <p class="mt-2 text-slate-600 dark:text-slate-300">Perfect for open source projects</p>
            <div class="mt-6">
              <span class="text-5xl font-bold text-slate-900 dark:text-white">Free</span>
            </div>
            <p class="mt-2 text-sm text-slate-600 dark:text-slate-300">Forever free for open source projects</p>
          </div>
          
          <div class="mt-8">
            <ul class="space-y-4">
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">AI documentation generation</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">Auto-sync with code changes</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">Basic CI/CD integration</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">Community support</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">Up to 3 repositories</span>
              </li>
            </ul>
          </div>
          
          <div class="mt-8">
            <a href="#contact" class="block w-full rounded-lg border border-brand-600 bg-white px-4 py-3 text-center text-sm font-semibold text-brand-600 transition hover:bg-brand-50 dark:bg-slate-800 dark:text-brand-400 dark:hover:bg-slate-700">
              Get Started Free
            </a>
          </div>
        </div>

        <!-- Enterprise Tier -->
        <div class="relative rounded-2xl border-2 border-brand-600 bg-white p-8 shadow-lg dark:border-brand-500 dark:bg-slate-800">
          <!-- Popular badge -->
          <div class="absolute -top-4 left-1/2 -translate-x-1/2">
            <span class="rounded-full bg-brand-600 px-4 py-1 text-sm font-semibold text-white dark:bg-brand-500">
              Most Popular
            </span>
          </div>
          
          <div class="text-center">
            <h3 class="text-2xl font-bold text-slate-900 dark:text-white">Enterprise</h3>
            <p class="mt-2 text-slate-600 dark:text-slate-300">For organizations that need it all</p>
            <div class="mt-6">
              <span class="text-5xl font-bold text-slate-900 dark:text-white">$129</span>
              <span class="text-xl text-slate-600 dark:text-slate-300">/month</span>
            </div>
            <p class="mt-2 text-sm text-slate-600 dark:text-slate-300">Everything you need, nothing you don't</p>
          </div>
          
          <div class="mt-8">
            <ul class="space-y-4">
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">Everything in Open Source</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">Unlimited repositories</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">Totally custom features for your org</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">SSO integration (if desired)</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">Priority support & onboarding</span>
              </li>         
              <li class="flex items-start">
                <svg class="h-5 w-5 text-brand-600 mt-0.5 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                <span class="text-slate-600 dark:text-slate-300">Dedicated account manager</span>
              </li>
            </ul>
          </div>
          
          <div class="mt-8">
            <a href="#contact" class="block w-full rounded-lg bg-brand-600 px-4 py-3 text-center text-sm font-semibold text-white shadow-glow transition hover:bg-brand-700 focus:outline-none focus-visible:ring-2 focus-visible:ring-brand-500/60">
              Start Enterprise Trial
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- FAQ Section -->
  <section class="bg-amber-50 py-16 dark:bg-slate-900">
    <div class="container mx-auto px-6">
      <div class="mx-auto max-w-3xl">
        <h2 class="text-center text-3xl font-bold text-slate-900 dark:text-white">Frequently Asked Questions</h2>
        <div class="mt-12 space-y-8">
          <div>
            <h3 class="text-lg font-semibold text-slate-900 dark:text-white">What counts as an open source project?</h3>
            <p class="mt-2 text-slate-600 dark:text-slate-300">Any project with a public repository that has an open source license (MIT, Apache, GPL, etc.) qualifies for our free tier.</p>
          </div>
          <div>
            <h3 class="text-lg font-semibold text-slate-900 dark:text-white">Can I switch plans anytime?</h3>
            <p class="mt-2 text-slate-600 dark:text-slate-300">Yes! You can upgrade or downgrade your plan at any time. Changes take effect immediately, and we'll prorate any billing differences.</p>
          </div>
          <div>
            <h3 class="text-lg font-semibold text-slate-900 dark:text-white">What kind of custom features can you build?</h3>
            <p class="mt-2 text-slate-600 dark:text-slate-300">We can build custom integrations with your existing tools, specialized documentation templates, custom CI/CD workflows, and any other features that fit your organization's specific needs.</p>
          </div>
          <div>
            <h3 class="text-lg font-semibold text-slate-900 dark:text-white">Is there a setup fee?</h3>
            <p class="mt-2 text-slate-600 dark:text-slate-300">No setup fees, no hidden costs. What you see is what you pay. We'll help you get started at no extra charge.</p>
          </div>
          <div>
            <h3 class="text-lg font-semibold text-slate-900 dark:text-white">What if I'm not satisfied?</h3>
            <p class="mt-2 text-slate-600 dark:text-slate-300">We offer a 30-day money-back guarantee. If you're not completely satisfied with DocFlow, we'll refund your payment, no questions asked.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA Section -->
  <section id="contact" class="py-20">
    <div class="container mx-auto px-6">
      <div class="mx-auto max-w-3xl text-center">
        <h2 class="text-3xl font-bold text-slate-900 dark:text-white">Ready to get started?</h2>
        <p class="mt-4 text-xl text-slate-600 dark:text-slate-300">
          Book a call with our team to discuss your needs and see how DocFlow can help your organization.
        </p>
        <div class="mt-8">
          <a href="/book-a-call" class="inline-flex items-center justify-center rounded-lg bg-brand-600 px-6 py-4 text-lg font-semibold text-white shadow-glow transition hover:bg-brand-700 focus:outline-none focus-visible:ring-2 focus-visible:ring-brand-500/60">
            Book a Call
            <svg class="ml-2 h-5 w-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </a>
        </div>
        <p class="mt-4 text-sm text-slate-500 dark:text-slate-400">
          No commitment required • 30-minute consultation • Free setup assistance • 30-day money-back guarantee
        </p>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <Footer {currentYear} />
</div>
