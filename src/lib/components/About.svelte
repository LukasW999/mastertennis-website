<script lang="ts">
  import { base } from '$app/paths';
</script>

<section id="about" class="py-24 bg-dark-surface border-t border-white/5">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
      <div class="relative">
        <div class="absolute inset-0 bg-neon-orange translate-x-4 translate-y-4 z-0"></div>
        <img src="{base}/profile.png" alt="Max Wenzel - Tennistrainer" class="relative z-10 w-full h-auto grayscale hover:grayscale-0 transition-all duration-500 object-cover aspect-[4/5]" />
      </div>
      
      <div>
        <h2 class="text-5xl md:text-7xl font-black text-white uppercase tracking-tighter mb-8">
          Max <br/><span class="text-neon-orange">Wenzel</span>
        </h2>
        <div class="space-y-6 text-lg text-text-muted">
          <p>
            Ich bin Max, 27 Jahre alt und lebe für den Tennissport. Seit meinem 16. Lebensjahr stehe ich als Trainer auf dem Platz und gebe meine Leidenschaft und Erfahrung an Spieler jeder Spielstärke weiter.
          </p>
          <p>
            Als Vereinstrainer beim <strong class="text-white">Tennis Club Wörth am Main</strong> und dem <strong class="text-white">Tennis Club Nieder Roden</strong> betreue ich Mannschaften und Einzelspieler.
          </p>
          <div class="p-6 bg-dark-bg border-l-4 border-volt-yellow mt-8 shadow-xl">
            <h3 class="text-volt-yellow font-bold uppercase text-xl mb-2">Mein Fokus: Privatstunden</h3>
            <p class="text-sm">
              In meinen 1-zu-1 Sessions legen wir den Schalter um. Intensive Drills, taktisches Verständnis und Technik-Tuning sorgen für schnelle Fortschritte und extrem zufriedene Kunden.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
