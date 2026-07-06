<script lang="ts">
  import Navigation from '$lib/components/Navigation.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
  <meta name="robots" content="noindex, nofollow">
  <title>Impressum | Mastertennis</title>
</svelte:head>

<Navigation />

<main class="pt-32 pb-24 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 min-h-screen">
  <div class="bg-dark-surface p-8 md:p-12 rounded-2xl border border-white/5 shadow-2xl legal-content">
    <div id='generator_results'>
      <div id='generator_results_content'>
        <h1>Impressum</h1>
        <h2>Verantwortliche(r)</h2>
        <p class='generator_user_input'>Maximilian Wenzel</p>
        <h3>Postanschrift</h3>
        <p class='generator_user_input'>63533 Mainhausen, Erzbergerstraße 6</p>
        <h3>Kontakt</h3>
        <p>E-Mail: mastertennis26 [at] gmail [punkt] com</p>
        <p>Telefon: 0152 - 55 32 18 43</p>
        <h2>Berufshaftpflichtversicherung</h2>
        <p class='generator_user_input'>Baloise Sachversicherung AG Deutschland<br />
        Basler Straße 4<br />
        61352 Bad Homburg v. d. Höhe</p>
        <h3>Geltungsbereich des Versicherungsschutzes</h3>
        <p class='generator_user_input'>Deutschland</p>
        <h2>Hinweise zur Website</h2>
        <h3>Urheberrechtliche Hinweise</h3>
        <p class='generator_user_input'>https://weiss-blau-woerth.de<br />
        https://1tcn.de</p>
        <h3>Verantwortlich für journalistisch-redaktionelle Inhalte</h3>
        <p class='generator_user_input'>[Bitte Informationen ergänzen]</p>
        <h2>Information gemäß § 36 VSBG</h2>
        <p>Gemäß § 36 VSBG (Verbraucherstreitbeilegungsgesetz – Gesetz über die alternative Streitbeilegung in Verbrauchersachen) erklärt der Betreiber dieser Website:</p>
        <p>Wir sind weder bereit noch verpflichtet, an Streitbeilegungsverfahren vor einer Verbraucherschlichtungsstelle teilzunehmen.</p>
        <p><em>Dieses Impressum wurde mit Hilfe des <a href="https://www.activemind.de/generatoren/impressum/" target="_blank" rel="noopener">Impressums-Generators der activeMind AG</a> erstellt (Version 2024-07-21).</em></p>
      </div>
    </div>
  </div>
</main>

<Footer />

<style>
  :global(.legal-content) {
    color: #e5e7eb;
  }
  :global(.legal-content h1) {
    font-size: 2.25rem;
    font-weight: 900;
    color: white;
    margin-bottom: 2rem;
    text-transform: uppercase;
    letter-spacing: -0.05em;
  }
  :global(.legal-content h2) {
    font-size: 1.5rem;
    font-weight: 700;
    color: white;
    margin-top: 3rem;
    margin-bottom: 1.5rem;
    text-transform: uppercase;
    letter-spacing: 0.025em;
  }
  :global(.legal-content h3) {
    font-size: 1.25rem;
    font-weight: 700;
    color: white;
    margin-top: 2rem;
    margin-bottom: 1rem;
  }
  :global(.legal-content h4) {
    font-size: 1.125rem;
    font-weight: 700;
    color: white;
    margin-top: 1.5rem;
    margin-bottom: 0.75rem;
  }
  :global(.legal-content p) {
    margin-bottom: 1.5rem;
    line-height: 1.75;
  }
  :global(.legal-content ul) {
    list-style-type: disc;
    list-style-position: inside;
    margin-bottom: 1.5rem;
  }
  :global(.legal-content li) {
    margin-bottom: 0.5rem;
  }
  :global(.legal-content a) {
    color: #ff5500; /* neon-orange */
    text-decoration: underline;
    transition: color 0.2s ease-in-out;
  }
  :global(.legal-content a:hover) {
    color: white;
  }
  :global(.legal-content .generator_user_input) {
    font-weight: 700;
    color: white;
    background-color: rgba(255, 255, 255, 0.05);
    padding: 0.5rem 1rem;
    border-radius: 0.25rem;
    border-left: 3px solid #ff5500;
  }
</style>
