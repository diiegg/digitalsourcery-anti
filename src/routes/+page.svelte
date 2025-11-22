<script lang="ts">
  import Button from '$lib/components/Button.svelte';
  import Card from '$lib/components/Card.svelte';
  import Section from '$lib/components/Section.svelte';

  // Svelte 5 Runes
  let count = $state(0);

  function castSpell() {
    count += 1;
  }
</script>

<!-- Hero Section -->
<Section class="min-h-[90vh] flex items-center justify-center text-center">
  <div class="max-w-4xl mx-auto">
    <h1 class="text-6xl md:text-8xl text-transparent bg-clip-text bg-gradient-to-r from-mana to-arcane drop-shadow-[0_0_10px_rgba(0,243,255,0.5)] mb-8 animate-pulse-slow">
      Digital Sorcery
    </h1>
    
    <p class="text-xl md:text-2xl text-gray-400 max-w-2xl mx-auto mb-12 font-light leading-relaxed">
      Weaving ancient code into modern infrastructure. <br>
      <span class="text-mana">Platform Engineering</span> & <span class="text-arcane">Automation Consulting</span>.
    </p>

    <div class="flex flex-col md:flex-row items-center justify-center gap-6">
      <Button href="/contact" variant="primary">
        Summon Us
      </Button>
      <Button href="/services" variant="secondary">
        Explore Grimoire
      </Button>
    </div>
  </div>
</Section>

<!-- About Section -->
<Section class="bg-white/5">
  <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
    <div>
      <h2 class="text-4xl text-white mb-6">The Technomancers</h2>
      <p class="text-gray-400 mb-6 leading-relaxed">
        In an age where infrastructure is code and deployment is a ritual, we are the arch-mages of the cloud. We don't just build platforms; we enchant them with self-healing properties, automated scaling, and impenetrable security wards.
      </p>
      <p class="text-gray-400 leading-relaxed">
        Our philosophy blends the disciplined study of ancient algorithms with the bleeding-edge sorcery of modern DevOps tools.
      </p>
    </div>
    <div class="relative h-64 md:h-96 rounded-lg overflow-hidden border border-mana/20 bg-black/50 flex items-center justify-center group">
      <div class="absolute inset-0 bg-gradient-to-br from-mana/10 to-arcane/10 group-hover:opacity-75 transition duration-500"></div>
      <div class="text-6xl text-mana/50 font-display">
        &lt;/&gt;
      </div>
    </div>
  </div>
</Section>

<!-- Services Preview -->
<Section>
  <div class="text-center mb-16">
    <h2 class="text-4xl text-white mb-4">Our Spells</h2>
    <p class="text-gray-400">Core competencies for the modern age.</p>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    <Card>
      <h3 class="text-xl text-gold mb-2">Platform Engineering</h3>
      <div class="h-1 w-12 bg-arcane rounded mb-4"></div>
      <p class="text-sm text-gray-400 font-mono mb-4">Internal Developer Platforms (IDP) that empower your wizards to cast spells faster.</p>
      <div class="text-mana text-xs uppercase tracking-wider">Kubernetes • Backstage</div>
    </Card>

    <Card>
      <h3 class="text-xl text-gold mb-2">Automation Sorcery</h3>
      <div class="h-1 w-12 bg-arcane rounded mb-4"></div>
      <p class="text-sm text-gray-400 font-mono mb-4">Self-correcting CI/CD pipelines that deploy with the precision of a clockwork golem.</p>
      <div class="text-mana text-xs uppercase tracking-wider">GitHub Actions • ArgoCD</div>
    </Card>

    <Card>
      <h3 class="text-xl text-gold mb-2">Cloud Architecture</h3>
      <div class="h-1 w-12 bg-arcane rounded mb-4"></div>
      <p class="text-sm text-gray-400 font-mono mb-4">Resilient infrastructure designed to withstand the chaotic energies of the internet.</p>
      <div class="text-mana text-xs uppercase tracking-wider">AWS • Terraform</div>
    </Card>
  </div>
  
  <div class="text-center mt-12">
    <Button href="/services" variant="ghost">View All Services &rarr;</Button>
  </div>
</Section>

<!-- CTA -->
<Section class="text-center">
  <div class="max-w-3xl mx-auto bg-gradient-to-r from-mana/10 to-arcane/10 border border-mana/20 rounded-2xl p-12">
    <h2 class="text-3xl text-white mb-6">Ready to Ascend?</h2>
    <p class="text-gray-400 mb-8">
      Your infrastructure awaits its transformation. Let us weave the spells that will secure your digital legacy.
    </p>
    <Button href="/contact" variant="primary">
      Begin the Ritual
    </Button>
  </div>
</Section>
