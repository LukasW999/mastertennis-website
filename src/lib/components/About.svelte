<script lang="ts">
  import { base } from '$app/paths';
  import { onMount } from 'svelte';

  const images = [
    `${base}/profile1.jpeg`,
    `${base}/profile2.jpeg`,
    `${base}/profile3.jpeg`
  ];
  let currentImageIndex = $state(0);

  onMount(() => {
    const interval = setInterval(() => {
      currentImageIndex = (currentImageIndex + 1) % images.length;
    }, 4000);
    return () => clearInterval(interval);
  });
</script>

<section id="about" class="py-24 bg-dark-surface border-t border-white/5">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
      <div class="relative w-full aspect-[4/5]">
        <div class="absolute inset-0 bg-neon-orange translate-x-4 translate-y-4 z-0"></div>
        {#each images as image, i}
          <img 
            src={image} 
            alt="Max Wenzel - Tennistrainer" 
            class="absolute top-0 left-0 z-10 w-full h-full object-cover transition-opacity duration-1000"
            style="opacity: {currentImageIndex === i ? 1 : 0}; pointer-events: {currentImageIndex === i ? 'auto' : 'none'};"
          />
        {/each}
      </div>
      
      <div>
        <h2 class="text-5xl md:text-7xl font-black text-white uppercase tracking-tighter mb-8">
          Verstehen. Trainieren. <br/><span class="text-neon-orange">Dominieren.</span>
        </h2>
        <div class="space-y-6 text-lg text-text-muted">
          <p>
            Ich bin Max, Tennistrainer und Gründer von <strong class="text-white">Master Tennis</strong>.
          </p>
          <p>
            Tennis begleitet mich seit meinem 9. Lebensjahr. Seit meinem 16. Lebensjahr stehe ich selbst als Trainer auf dem Platz und arbeite mit Kindern, Jugendlichen und Erwachsenen auf unterschiedlichen Spielniveaus – vom Anfänger bis zum ambitionierten Mannschaftsspieler.
          </p>
          <div class="p-6 bg-dark-bg border-l-4 border-volt-yellow mt-8 shadow-xl">
            <h3 class="text-volt-yellow font-bold uppercase text-xl mb-2">Mein Ansatz: Verstehen. Trainieren. Dominieren.</h3>
            <p class="text-sm">
              Ich möchte, dass du nicht einfach nur Bälle schlägst, sondern dein Spiel wirklich verstehst, gezielt trainierst und auf dem Platz selbstbewusster auftrittst. Technik, Taktik, Bewegung und Athletik gehören für mich zusammen – denn gutes Tennis entsteht nicht durch Zufall, sondern durch klares Training.
            </p>
          </div>
          <p>
            Durch meine Ausbildung zum Sport- und Gesundheitstrainer verbinde ich Tennistraining mit einem modernen Blick auf Bewegung, Koordination und Belastbarkeit.
          </p>
          <p>
            <strong class="text-white">Master Tennis</strong> steht für ehrliches Coaching, klare Struktur und Training, das dich wirklich weiterbringt.
          </p>
        </div>
      </div>
    </div>
  </div>
</section>
