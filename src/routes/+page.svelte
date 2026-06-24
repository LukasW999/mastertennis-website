<script lang="ts">
  import Navigation from '$lib/components/Navigation.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import About from '$lib/components/About.svelte';
  import Services from '$lib/components/Services.svelte';
  import Testimonials from '$lib/components/Testimonials.svelte';
  import Contact from '$lib/components/Contact.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
  <title>Mastertennis | Max Wenzel - Tennistrainer</title>
  <meta name="description" content="Professionelles Tennistraining für schnelle Fortschritte. Privat- und Gruppentraining in Wörth am Main und Nieder Roden." />
</svelte:head>

<div class="font-sans antialiased bg-dark-bg text-text-main selection:bg-neon-orange selection:text-white">
  <Navigation />
  
  <main>
    <Hero />
    <About />
    <Services />
    <Testimonials />
    <Contact />
  </main>

  <Footer />
</div>
