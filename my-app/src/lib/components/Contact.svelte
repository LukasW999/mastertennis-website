<script lang="ts">
</script>

<section id="contact" class="py-24 bg-neon-orange relative overflow-hidden">
  <div class="absolute -right-40 -top-40 w-96 h-96 bg-volt-yellow rounded-full blur-3xl opacity-20"></div>
  
  <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
    <div class="text-center mb-12">
      <h2 class="text-5xl md:text-7xl font-black text-dark-bg uppercase tracking-tighter">
        Bereit für den <br/> <span class="text-white">nächsten Schritt?</span>
      </h2>
      <p class="mt-6 text-xl text-dark-bg font-medium">
        Schreib mir direkt und wir finden deinen perfekten Termin.
      </p>
    </div>

    <form action="https://api.web3forms.com/submit" method="POST" class="bg-dark-bg p-8 md:p-12 shadow-2xl">
      <!-- Web3Forms Access Key -->
      <input type="hidden" name="access_key" value="af52ccf4-c16d-4f23-b9c4-080bb2f58124">

      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
        <div>
          <label for="name" class="block text-sm font-bold text-text-muted uppercase tracking-wider mb-2">Name</label>
          <input type="text" id="name" name="name" required class="w-full bg-dark-surface border border-white/10 text-white px-4 py-3 focus:outline-none focus:border-volt-yellow focus:ring-1 focus:ring-volt-yellow transition-colors">
        </div>
        <div>
          <label for="email" class="block text-sm font-bold text-text-muted uppercase tracking-wider mb-2">E-Mail</label>
          <input type="email" id="email" name="email" required class="w-full bg-dark-surface border border-white/10 text-white px-4 py-3 focus:outline-none focus:border-volt-yellow focus:ring-1 focus:ring-volt-yellow transition-colors">
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
        <div>
          <label for="type" class="block text-sm font-bold text-text-muted uppercase tracking-wider mb-2">Trainingsart</label>
          <select id="type" name="type" required class="w-full bg-dark-surface border border-white/10 text-white px-4 py-3 focus:outline-none focus:border-volt-yellow focus:ring-1 focus:ring-volt-yellow transition-colors appearance-none">
            <option value="" disabled selected>Bitte wählen...</option>
            <option value="Einzeltraining">Einzeltraining</option>
            <option value="Gruppentraining">Gruppentraining</option>
          </select>
        </div>
        <div>
          <label for="level" class="block text-sm font-bold text-text-muted uppercase tracking-wider mb-2">Spiel Level</label>
          <select id="level" name="level" required class="w-full bg-dark-surface border border-white/10 text-white px-4 py-3 focus:outline-none focus:border-volt-yellow focus:ring-1 focus:ring-volt-yellow transition-colors appearance-none">
            <option value="" disabled selected>Bitte wählen...</option>
            <option value="Anfänger">Anfänger</option>
            <option value="Fortgeschritten">Fortgeschritten</option>
            <option value="Turnierspieler">Turnierspieler</option>
          </select>
        </div>
      </div>

      <div class="mb-8">
        <label for="message" class="block text-sm font-bold text-text-muted uppercase tracking-wider mb-2">Nachricht</label>
        <textarea id="message" name="message" rows="4" required class="w-full bg-dark-surface border border-white/10 text-white px-4 py-3 focus:outline-none focus:border-volt-yellow focus:ring-1 focus:ring-volt-yellow transition-colors resize-none"></textarea>
      </div>

      <button type="submit" class="w-full bg-volt-yellow text-dark-bg text-xl font-black uppercase tracking-widest py-5 hover:bg-white transition-colors duration-300">
        Jetzt anfragen
      </button>
    </form>
  </div>
</section>
