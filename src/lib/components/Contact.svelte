<script lang="ts">
  import { base } from '$app/paths';
  import { fly } from 'svelte/transition';

  let accepted = $state(false);
  let isSubmitting = $state(false);
  let showSuccess = $state(false);
  let errorMessage = $state('');

  async function handleSubmit(event: Event) {
    event.preventDefault();
    isSubmitting = true;
    errorMessage = '';

    const form = event.target as HTMLFormElement;
    const formData = new FormData(form);

    try {
      const response = await fetch('https://api.web3forms.com/submit', {
        method: 'POST',
        body: formData
      });
      const data = await response.json();
      
      if (data.success) {
        showSuccess = true;
        form.reset();
        accepted = false;
        setTimeout(() => { showSuccess = false; }, 5000);
      } else {
        errorMessage = data.message || 'Ein Fehler ist aufgetreten. Bitte versuche es später noch einmal.';
        setTimeout(() => { errorMessage = ''; }, 5000);
      }
    } catch (e) {
      errorMessage = 'Verbindungsfehler. Bitte überprüfe deine Internetverbindung.';
      setTimeout(() => { errorMessage = ''; }, 5000);
    } finally {
      isSubmitting = false;
    }
  }
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

    <form onsubmit={handleSubmit} class="bg-dark-bg p-8 md:p-12 shadow-2xl relative">
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
            <option value="Vereinstraining">Vereinstraining</option>
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

      <div class="mb-8 flex items-start gap-3">
        <input type="checkbox" id="privacy" name="privacy" bind:checked={accepted} required class="mt-1 h-4 w-4 accent-volt-yellow cursor-pointer">
        <label for="privacy" class="text-sm text-text-muted cursor-pointer select-none leading-relaxed">
          Ich stimme zu, dass meine Angaben aus dem Kontaktformular zur Beantwortung meiner Anfrage erhoben und verarbeitet werden. Ich habe die <a href="{base}/datenschutz" target="_blank" class="text-white hover:text-volt-yellow underline transition-colors">Datenschutzerklärung</a> gelesen und akzeptiere diese. *
        </label>
      </div>

      <button type="submit" disabled={!accepted || isSubmitting} class="w-full bg-volt-yellow text-dark-bg text-xl font-black uppercase tracking-widest py-5 hover:bg-white transition-colors duration-300 disabled:opacity-40 disabled:cursor-not-allowed disabled:hover:bg-volt-yellow h-[68px] flex items-center justify-center">
        {#if isSubmitting}
          <svg class="animate-spin h-6 w-6 text-dark-bg" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
            <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
            <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
          </svg>
        {:else}
          Jetzt anfragen
        {/if}
      </button>
    </form>
  </div>

  {#if showSuccess}
    <div transition:fly={{ y: 50, duration: 300 }} class="fixed bottom-6 right-6 md:bottom-10 md:right-10 bg-volt-yellow text-dark-bg px-6 py-4 shadow-2xl border-l-8 border-neon-orange z-50 flex items-center gap-3 font-bold text-lg max-w-sm">
      <svg class="w-6 h-6 text-neon-orange flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path></svg>
      Anfrage erfolgreich gesendet!
    </div>
  {/if}

  {#if errorMessage}
    <div transition:fly={{ y: 50, duration: 300 }} class="fixed bottom-6 right-6 md:bottom-10 md:right-10 bg-red-600 text-white px-6 py-4 shadow-2xl border-l-8 border-dark-bg z-50 flex items-center gap-3 font-bold text-lg max-w-sm">
      <svg class="w-6 h-6 flex-shrink-0 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M6 18L18 6M6 6l12 12"></path></svg>
      {errorMessage}
    </div>
  {/if}
</section>
