<script lang="ts">
  const currentYear = new Date().getFullYear();
</script>

<footer class="bg-dark-bg border-t border-white/10 py-12">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row items-center justify-between">
    <div class="mb-4 md:mb-0">
      <a href="#" class="text-2xl font-black text-white tracking-tighter uppercase italic">
        Master<span class="text-neon-orange">tennis</span>
      </a>
    </div>
    
    <div class="text-text-muted text-sm flex space-x-6">
      <a href="#" class="hover:text-white transition-colors">Impressum</a>
      <a href="#" class="hover:text-white transition-colors">Datenschutz</a>
    </div>
  </div>
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-8 text-center text-xs text-text-muted/50">
    &copy; {currentYear} Mastertennis - Max Wenzel. Alle Rechte vorbehalten.
  </div>
</footer>
