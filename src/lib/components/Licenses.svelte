<script lang="ts">
  const licenses = [
    { name: "medizinisches Fitnesstraining", level: "A-Lizenz", colorClass: "text-volt-yellow", borderHoverClass: "hover:border-volt-yellow", bgClass: "bg-volt-yellow/10", borderClass: "border-volt-yellow/20" },
    { name: "Rückentraining", level: "A-Lizenz", colorClass: "text-volt-yellow", borderHoverClass: "hover:border-volt-yellow", bgClass: "bg-volt-yellow/10", borderClass: "border-volt-yellow/20" },
    { name: "Personal Training", level: "A-Lizenz", colorClass: "text-volt-yellow", borderHoverClass: "hover:border-volt-yellow", bgClass: "bg-volt-yellow/10", borderClass: "border-volt-yellow/20" },
    { name: "Bodybuilding", level: "A-Lizenz", colorClass: "text-volt-yellow", borderHoverClass: "hover:border-volt-yellow", bgClass: "bg-volt-yellow/10", borderClass: "border-volt-yellow/20" },
    { name: "Fitnesstraining", level: "A-Lizenz", colorClass: "text-volt-yellow", borderHoverClass: "hover:border-volt-yellow", bgClass: "bg-volt-yellow/10", borderClass: "border-volt-yellow/20" },
    { name: "Sporternährung", level: "B-Lizenz", colorClass: "text-neon-orange", borderHoverClass: "hover:border-neon-orange", bgClass: "bg-neon-orange/10", borderClass: "border-neon-orange/20" },
    { name: "Tennis Trainer", level: "Assistenztrainer", colorClass: "text-bright-cyan", borderHoverClass: "hover:border-bright-cyan", bgClass: "bg-bright-cyan/10", borderClass: "border-bright-cyan/20" }
  ];
</script>

<section id="licenses" class="py-24 bg-dark-bg border-t border-white/5 relative overflow-hidden">
  <div class="absolute -left-40 top-20 w-96 h-96 bg-bright-cyan rounded-full blur-[120px] opacity-10"></div>
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
    <div class="text-center mb-16">
      <h2 class="text-4xl md:text-6xl font-black text-white uppercase tracking-tighter">
        Qualifikation & <span class="text-neon-orange">Lizenzen</span>
      </h2>
      <p class="mt-4 text-xl text-text-muted max-w-2xl mx-auto">
        Ich bin zertifizierter <strong class="text-white">Sport- und Gesundheitstrainer</strong> mit fundiertem Fachwissen für dein bestes Training.
      </p>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
      {#each licenses as license}
        <div class="bg-dark-surface p-6 border border-white/5 transition-colors group flex flex-col justify-between {license.borderHoverClass}">
          <div>
            <div class="{license.colorClass} mb-4 transform group-hover:scale-110 transition-transform origin-left">
              <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"></path></svg>
            </div>
            <h3 class="text-xl font-bold text-white mb-2 leading-tight">{license.name}</h3>
          </div>
          <div class="inline-block mt-6 px-3 py-1 text-sm font-black uppercase tracking-wider w-fit border {license.bgClass} {license.colorClass} {license.borderClass}">
            {license.level}
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>
