<script lang="ts">
  import WaitlistModal from '$lib/components/WaitlistModal.svelte';
  import ProductCard from '$lib/components/ProductCard.svelte';
  import SEO from '$lib/components/SEO.svelte';
  import { secureStackVision, secureStackProducts, studioLabProducts, getSecureStackProductsByPhase } from '$lib/config/products';
  import type { StudioLabProduct } from '$lib/config/products';

  let isWaitlistOpen = false;
  let selectedProduct = '';
  let selectedProductId = '';

  function openWaitlist(productName: string, productId: string) {
    selectedProduct = productName;
    selectedProductId = productId;
    isWaitlistOpen = true;
  }
</script>

<SEO
	title="Products"
	description="Explore Thiru AI Labs' AI-native cybersecurity compliance suite: SecureStack. PolicyForge, CipherScan, and more."
/>

<WaitlistModal
  bind:isOpen={isWaitlistOpen}
  productName={selectedProduct || 'Thiru AI Labs'}
  productId={selectedProductId}
/>

<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
  
  <!-- ============================================
       PAGE HEADER / HERO
       ============================================ -->
  <div class="mb-16">
    <h1 class="text-2xl md:text-3xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      AI-Native Cybersecurity Compliance
    </h1>
    <div class="max-w-none">
      <p class="text-lg text-neutral-600 dark:text-neutral-400 leading-relaxed">
        We build SecureStack — a modular suite that helps regulated SMBs and defense supply chain partners achieve compliance faster. From policy generation to cryptographic scanning, everything you need for audit readiness in one integrated platform.
      </p>
    </div>
  </div>

  <!-- ============================================
       SECURESTACK SUITE SECTION
       ============================================ -->
  <section class="mb-16">
    <h2 id="secure-stack" class="text-2xl font-bold text-neutral-900 dark:text-[#fedf19] mb-6">
      SecureStack — The Suite
    </h2>
    
    <div class="grid md:grid-cols-1 gap-6 items-stretch">
      
      <!-- SecureStack Suite -->
      <ProductCard 
        title={secureStackVision.title}
        status={secureStackVision.status}
        statusBg={secureStackVision.statusBg}
        statusText={secureStackVision.statusText}
        padding="p-8"
        titleSize="text-2xl"
        faded={false}
      >
        <p class="text-neutral-700 dark:text-neutral-400 leading-relaxed mb-8">
          {@html secureStackVision.description}
        </p>

        {#each secureStackVision.phases as phase}
          <!-- Phase {phase.number} -->
          <div class="mb-10">
            <div class="flex items-center gap-3 mb-4">
              <div class="h-8 w-8 rounded-full bg-[#fe1817] text-white flex items-center justify-center text-sm font-bold">{phase.number}</div>
              <h4 class="text-sm font-semibold text-neutral-700 dark:text-neutral-300">{phase.title}</h4>
            </div>
            
            <div class="grid md:grid-cols-2 gap-4">
              {#each getSecureStackProductsByPhase(phase.number) as product}
                <div class="bg-neutral-50 dark:bg-neutral-800 rounded-lg p-5 border border-neutral-200 dark:border-neutral-700">
                  <h4 class="font-semibold text-neutral-900 dark:text-neutral-100 mb-2">{product.title}</h4>
                  <p class="text-neutral-600 dark:text-neutral-400 text-sm mb-4">
                    {product.shortDescription}
                  </p>
                  <div class="flex gap-2">
                    <a
                      href="/products/{product.slug}"
                      class="inline-flex items-center gap-1 px-3 py-1.5 bg-[#202020] dark:bg-neutral-700 text-white text-sm font-medium rounded-md hover:bg-[#fedf19] hover:text-[#fe1817] transition-colors"
                    >
                      Learn more
                      <svg class="w-3 h-3 shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                      </svg>
                    </a>
                    {#if product.status === 'Building'}
                      <button
                        on:click={() => openWaitlist(product.title, product.waitlistId)}
                        class="inline-flex items-center gap-1 px-3 py-1.5 bg-[#fe1817] text-white text-sm font-medium rounded-md hover:bg-[#fedf19] hover:text-[#fe1817] transition-colors"
                      >
                        Join waitlist
                        <svg class="w-3 h-3 shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                        </svg>
                      </button>
                    {/if}
                  </div>
                </div>
              {/each}
            </div>
          </div>
        {/each}

        <!-- Strategic Fit -->
        <div class="border-t border-neutral-200 dark:border-neutral-700 pt-6 mb-6">
          <h4 class="text-sm font-semibold text-neutral-700 dark:text-neutral-300 mb-3">
            Strategic Fit
          </h4>
          <p class="text-neutral-600 dark:text-neutral-400 text-sm leading-relaxed mb-4">
            {secureStackVision.strategicFit}
          </p>
          <p class="text-neutral-600 dark:text-neutral-400 text-sm leading-relaxed">
            <strong>Why we're different:</strong> {secureStackVision.differentiator}
          </p>
        </div>

        <!-- Build in Public CTA -->
        <div class="bg-blue-50 dark:bg-blue-900/20 border border-blue-200 dark:border-blue-800 rounded-lg p-4 mb-6">
          <p class="text-sm text-blue-900 dark:text-blue-100">
            <strong>Follow the build journey:</strong> We ship in public on 
            <a href="https://www.linkedin.com/in/nick-thiru" target="_blank" class="underline hover:no-underline font-semibold">
              LinkedIn
            </a>
            {' '}and 
            <a href="https://x.com/nickthiru" target="_blank" class="underline hover:no-underline font-semibold">
              X/Twitter
            </a>
            {' '}— see exactly how this product evolves.
          </p>
        </div>

        {#snippet footer()}
          <div class="space-y-2">
            <p class="text-sm text-neutral-500 dark:text-neutral-400 italic">
              <strong>Timeline:</strong> {secureStackVision.timeline}
            </p>
            <p class="text-sm text-neutral-500 dark:text-neutral-400 italic">
              {secureStackVision.timelineNote}
            </p>
          </div>
        {/snippet}
      </ProductCard>

    </div>
  </section>

  <!-- ============================================
       STUDIO LAB — OTHER EXPLORATIONS SECTION
       ============================================ -->
  <section class="mb-16">
    <h2 class="text-xl font-bold text-neutral-900 dark:text-[#fedf19] mb-4">
      Studio Lab — Other Explorations
    </h2>
    <p class="text-neutral-600 dark:text-neutral-400 mb-6 max-w-3xl">
      Projects we've explored but aren't actively developing right now. Some may return in the future.
    </p>
    
    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-4">
      {#each studioLabProducts as product}
        <div class="bg-neutral-50 dark:bg-neutral-800/50 border border-neutral-200 dark:border-neutral-700 rounded-lg p-5 opacity-75">
          <h3 class="text-lg font-semibold text-neutral-700 dark:text-neutral-300 mb-2">
            {product.title}
          </h3>
          <p class="text-sm text-neutral-500 dark:text-neutral-400 leading-relaxed">
            {product.shortDescription}
          </p>
        </div>
      {/each}
    </div>
    
    <!-- Optional: Single email capture for notifications -->
    <div class="mt-6 p-4 bg-neutral-100 dark:bg-neutral-800/30 border border-neutral-200 dark:border-neutral-700 rounded-lg">
      <p class="text-sm text-neutral-600 dark:text-neutral-400">
        <strong>Want to know if these projects come back?</strong> Follow us on 
        <a href="https://www.linkedin.com/in/nick-thiru" target="_blank" class="text-[#fe1817] hover:underline font-medium">LinkedIn</a>
        {' '}or 
        <a href="https://x.com/nickthiru" target="_blank" class="text-[#fe1817] hover:underline font-medium">X/Twitter</a>
        {' '}for updates on all our work.
      </p>
    </div>
  </section>

</div>
