<script>
  import SectionLabel from './SectionLabel.svelte';
</script>

<section class="bg-[#f5f5f5] px-6 py-24">
  <div class="max-w-[1400px] mx-auto grid grid-cols-1 lg:grid-cols-12 gap-12">
    <div class="lg:col-span-3">
      <SectionLabel label="Why Mastermind" />
    </div>
    
    <div class="lg:col-span-9 grid grid-cols-1 md:grid-cols-2 gap-16">
      <div>
        <h2 class="font-serif text-3xl md:text-4xl leading-tight text-gray-900 mb-6">
          Mastermind delivers seven-figure wealth through proven investment strategies
        </h2>
        <p class="text-gray-500 leading-relaxed">
          We help busy professionals capture the $3 trillion wealth transfer in crypto, AI, and robotics—without the endless research. Get personalized portfolio guidance and proven 100x strategies with just 5 hours per week.
        </p>
      </div>
      
      <div class="flex gap-12 items-end pb-2">
        <div class="flex flex-col gap-1">
            <span class="text-4xl font-bold text-gray-900">100x</span>
            <span class="text-xs text-gray-400">proven strategies</span>
        </div>
        <div class="flex flex-col gap-1">
            <span class="text-4xl font-bold text-gray-900">5hrs</span>
            <span class="text-xs text-gray-400">weekly commitment</span>
        </div>
      </div>
    </div>
  </div>
</section>
