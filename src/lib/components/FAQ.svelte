<script lang="ts">
  import { slide } from 'svelte/transition';
  
  interface FAQItem {
    question: string;
    answer: string;
  }

  const faqs: FAQItem[] = [
    { question: "How much time do I need to commit each week?", answer: "Mastermind is designed for busy professionals. You only need to commit 5 hours per week to stay informed and implement our proven strategies. We handle the research so you can focus on execution." },
    { question: "What makes Mastermind's strategies proven?", answer: "Our strategies are based on proven 100x returns in crypto, AI, and robotics markets. We focus on capturing the $3 trillion wealth transfer happening now, using tested approaches that have generated seven-figure wealth for our members." },
    { question: "Do I need prior investment experience?", answer: "While Mastermind is designed for professionals with capital, you don't need to be an investment expert. Our personalized guidance walks you through each strategy, making sophisticated investing accessible even if you lack time for deep research." },
    { question: "What's included in the membership?", answer: "Members get personalized portfolio guidance, weekly market insights, access to proven 100x strategies, and entry to our exclusive community of successful professionals and millionaire members. Everything you need to scale your wealth in crypto, AI, and robotics." },
    { question: "How is this different from other investment services?", answer: "Unlike generic investment advice or time-consuming research platforms, Mastermind delivers done-for-you portfolio guidance specifically for busy professionals. We focus on high-growth opportunities in crypto, AI, and robotics with just a 5-hour weekly commitment." },
    { question: "Can I start with any amount of capital?", answer: "Mastermind is designed for professionals with capital ready to scale. While there's no strict minimum, our strategies work best for those prepared to make meaningful investments in high-growth opportunities." },
    { question: "How do I get started?", answer: "Simply join Mastermind to get immediate access to our community, personalized guidance, and proven strategies. You'll start receiving weekly insights and portfolio recommendations right away." }
  ];

  let openIndex: number | null = null;

  function toggle(index: number) {
    openIndex = openIndex === index ? null : index;
  }
</script>

<section class="bg-[#f5f5f5] px-6 py-24">
  <div class="max-w-[1400px] mx-auto grid grid-cols-1 lg:grid-cols-12 gap-12">
    <div class="lg:col-span-4">
      <h2 class="font-serif text-4xl text-gray-900 mb-6">
        Frequently asked questions
      </h2>
      <a href="/" class="text-sm text-gray-900 border-b border-gray-300 pb-0.5 hover:border-black transition-colors">See all support</a>
    </div>
    
    <div class="lg:col-span-8">
      <div class="border-t border-gray-200">
        {#each faqs as faq, i}
          <div class="border-b border-gray-200">
            <button 
              class="w-full py-6 flex justify-between items-center text-left hover:bg-gray-50 transition-colors"
              on:click={() => toggle(i)}
            >
              <span class="text-lg text-gray-800">{faq.question}</span>
              <span class="text-2xl font-light text-gray-400 ml-4">
                {openIndex === i ? '−' : '+'}
              </span>
            </button>
            {#if openIndex === i}
              <div transition:slide class="pb-6 text-gray-500 leading-relaxed">
                {faq.answer}
              </div>
            {/if}
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>
