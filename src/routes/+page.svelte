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
    <!-- Standard SEO -->
    <title>MASTERTENNIS | Max Wenzel - Professionelles Tennistraining</title>
    <meta name="description" content="Individuelles Tennistraining für alle Alters- und Leistungsklassen mit Max Wenzel. Einzel- & Gruppentraining beim TC Wörth am Main und TC Nieder Roden. Jetzt Probetraining vereinbaren!" />
    
    <!-- Meta Keywords -->
    <meta name="keywords" content="Tennistrainer, Tennis, Training, Einzelunterricht, TC Wörth am Main, TC Nieder Roden, Tennisschule" />

    <!-- Open Graph / Facebook / WhatsApp -->
    <meta property="og:site_name" content="MASTERTENNIS" />
    <meta property="og:type" content="website" />
    <meta property="og:url" content="https://mastertennis.de/" />
    <meta property="og:title" content="MASTERTENNIS | Max Wenzel - Professionelles Tennistraining" />
    <meta property="og:description" content="Verstehen, trainieren, dominieren. Individuelles Tennistraining beim TC Wörth am Main und TC Nieder Roden." />
    <meta property="og:image" content="https://mastertennis.de/profile.png" />

    <!-- Twitter -->
    <meta name="twitter:card" content="summary_large_image" />
    <meta name="twitter:url" content="https://mastertennis.de/" />
    <meta name="twitter:title" content="MASTERTENNIS | Max Wenzel" />
    <meta name="twitter:description" content="Verstehen, trainieren, dominieren." />
    <meta name="twitter:image" content="https://mastertennis.de/profile.png" />
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
