<script lang="ts">
  import { base } from "$app/paths";
</script>

<section
  id="references"
  class="py-24 bg-dark-surface border-t border-white/5 relative overflow-hidden"
>
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
    <div class="text-center mb-16">
      <h2
        class="text-5xl md:text-7xl font-black text-white uppercase tracking-tighter"
      >
        Vertrauen auf <br /> <span class="text-neon-orange">dem Platz</span>
      </h2>
    </div>

    <!-- Teil A: Vereine -->
    <div class="mb-24">
      <h3
        class="text-2xl font-bold text-text-muted uppercase tracking-widest text-center mb-8 inline-block w-full"
      >
        Meine Partner
      </h3>
      <div
        class="flex flex-col md:flex-row items-center justify-center gap-12 md:gap-24 transition-all duration-500"
      >
        <div class="flex flex-col items-center group">
          <div
            class="w-40 h-40 bg-white rounded-full flex items-center justify-center p-6 border-4 border-transparent group-hover:border-volt-yellow transition-colors shadow-lg mb-6"
          >
            <!-- Platzhalter für das Logo: Speichere das Bild als static/tc-woerth.png ab -->
            <img
              src="{base}/tc-woerth.png"
              alt="TC Wörth am Main"
              class="w-full h-full object-contain"
            />
          </div>
          <span class="text-xl font-black text-white uppercase tracking-wide"
            >TC Weiß-Blau Wörth</span
          >
        </div>
      </div>
    </div>

    <!-- Teil B: Review Cards -->
    <div>
      <h3
        class="text-2xl font-bold text-text-muted uppercase tracking-widest text-center mb-12"
      >
        Kundenstimmen
      </h3>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Card 1 -->
        <div
          class="bg-dark-bg p-8 border-l-4 border-neon-orange shadow-2xl relative group hover:-translate-y-2 transition-transform duration-300"
        >
          <div class="flex text-neon-orange mb-6">
            <!-- 5 Sterne -->
            {#each Array(5) as _}
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"
                ><path
                  d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"
                ></path></svg
              >
            {/each}
          </div>
          <p class="text-text-main italic mb-6">
            "Seit ich bei Max trainiere, hat sich meine Vorhand extrem
            verbessert. Die Intensität im Training ist genau das, was ich
            gebraucht habe. Absolut empfehlenswert!"
          </p>
          <div class="font-bold text-white uppercase tracking-wide text-sm">
            - Julian S.
          </div>
          <div class="text-xs text-text-muted mt-1">
            Privatkunde (Fortgeschritten)
          </div>
        </div>

        <!-- Card 2 -->
        <div
          class="bg-dark-bg p-8 border-l-4 border-volt-yellow shadow-2xl relative group hover:-translate-y-2 transition-transform duration-300"
        >
          <div class="flex text-volt-yellow mb-6">
            <!-- 5 Sterne -->
            {#each Array(5) as _}
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"
                ><path
                  d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"
                ></path></svg
              >
            {/each}
          </div>
          <p class="text-text-main italic mb-6">
            "Max holt in jeder Stunde 110% aus mir raus! Kein langes Gerede,
            sondern Fokus auf Taktik und Technik. Mein Aufschlag ist endlich
            eine Waffe."
          </p>
          <div class="font-bold text-white uppercase tracking-wide text-sm">
            - Thomas M.
          </div>
          <div class="text-xs text-text-muted mt-1">Turnierspieler</div>
        </div>

        <!-- Card 3 -->
        <div
          class="bg-dark-bg p-8 border-l-4 border-bright-cyan shadow-2xl relative group hover:-translate-y-2 transition-transform duration-300"
        >
          <div class="flex text-bright-cyan mb-6">
            <!-- 5 Sterne -->
            {#each Array(5) as _}
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"
                ><path
                  d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"
                ></path></svg
              >
            {/each}
          </div>
          <p class="text-text-main italic mb-6">
            "Wahnsinnige Energie! Selbst nach einem langen Arbeitstag schafft es
            Max, mich nochmal komplett zu motivieren. Das beste Training, das
            ich je hatte."
          </p>
          <div class="font-bold text-white uppercase tracking-wide text-sm">
            - Sarah K.
          </div>
          <div class="text-xs text-text-muted mt-1">Privatkundin</div>
        </div>
      </div>
    </div>
  </div>
</section>
