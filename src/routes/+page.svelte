<script lang="ts">
  import Button from "$lib/components/Button.svelte";
  import Card from "$lib/components/Card.svelte";
  import Section from "$lib/components/Section.svelte";

  // Svelte 5 Runes
  let count = $state(0);

  function castSpell() {
    count += 1;
  }
</script>

<svelte:head>
  <title>Digital Sorcery | Solarpunk Architecture</title>
</svelte:head>

<!-- Hero Section -->
<Section class="min-h-[90vh] flex items-center justify-center text-center">
  <div class="max-w-5xl mx-auto relative">
    <!-- Floating geometric elements -->
    <div
      class="absolute -top-20 -left-20 w-64 h-64 bg-emerald/10 rounded-full blur-3xl animate-float"
    ></div>
    <div
      class="absolute -bottom-20 -right-20 w-64 h-64 bg-energy/10 rounded-full blur-3xl animate-float"
      style="animation-delay: 2s"
    ></div>

    <h1
      class="text-7xl md:text-9xl font-display font-bold text-text mb-8 relative z-10 tracking-tight"
    >
      Digital <span
        class="text-transparent bg-clip-text bg-gradient-to-r from-emerald to-energy"
        >Sorcery</span
      >
    </h1>

    <p
      class="text-xl md:text-3xl text-silver max-w-3xl mx-auto mb-16 font-light leading-relaxed font-body"
    >
      Cultivating <span class="text-emerald font-medium"
        >organic infrastructure</span
      > for a utopian digital future.
    </p>

    <div
      class="flex flex-col md:flex-row items-center justify-center gap-8 relative z-10"
    >
      <Button href="/contact" variant="primary">Begin Transmutation</Button>
      <Button href="/services" variant="secondary">Consult the Grimoire</Button>
    </div>
  </div>
</Section>

<!-- About Section -->
<Section class="bg-white/30 backdrop-blur-sm">
  <div class="grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div class="order-2 md:order-1">
      <h2 class="text-5xl text-text mb-8 font-display">The Alchemists</h2>
      <p class="text-text/80 mb-6 leading-relaxed text-lg">
        We are architects of the solar age, blending ancient wisdom with
        futuristic technology. Our mission is to build digital ecosystems that
        are self-sustaining, resilient, and harmonious.
      </p>
      <p class="text-text/80 leading-relaxed text-lg">
        Like the alchemists of old, we transmute chaotic code into golden
        infrastructure, ensuring your platform grows organically with your
        vision.
      </p>
      <div class="mt-8 font-script text-4xl text-energy">
        As above, so below.
      </div>
    </div>
    <div
      class="order-1 md:order-2 relative h-96 rounded-2xl overflow-hidden shadow-2xl group"
    >
      <div
        class="absolute inset-0 bg-gradient-to-br from-emerald/20 to-energy/20 group-hover:scale-105 transition duration-700"
      ></div>
      <div class="absolute inset-0 flex items-center justify-center">
        <div
          class="w-32 h-32 border border-white/50 rounded-full flex items-center justify-center backdrop-blur-md"
        >
          <div class="w-24 h-24 border border-white/80 rotate-45"></div>
        </div>
      </div>
    </div>
  </div>
</Section>

<!-- Services Preview -->
<Section>
  <div class="text-center mb-20">
    <h2 class="text-5xl text-text mb-6 font-display">Elemental Arts</h2>
    <p class="text-silver text-lg">
      Mastering the forces of the digital ether.
    </p>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
    <Card>
      <div
        class="w-12 h-12 bg-emerald/10 rounded-full flex items-center justify-center mb-6 text-2xl"
      >
        🌱
      </div>
      <h3 class="text-2xl text-text font-display mb-4">Platform Ecology</h3>
      <p class="text-text/70 mb-6 leading-relaxed">
        Cultivating Internal Developer Platforms (IDP) that allow your team to
        flourish without friction.
      </p>
      <div class="text-emerald text-xs font-bold uppercase tracking-widest">
        Kubernetes • Backstage
      </div>
    </Card>

    <Card>
      <div
        class="w-12 h-12 bg-energy/10 rounded-full flex items-center justify-center mb-6 text-2xl"
      >
        ⚡
      </div>
      <h3 class="text-2xl text-text font-display mb-4">Automated Flow</h3>
      <p class="text-text/70 mb-6 leading-relaxed">
        Pipelines that flow like water, deploying code with natural precision
        and rhythm.
      </p>
      <div class="text-energy text-xs font-bold uppercase tracking-widest">
        GitHub Actions • ArgoCD
      </div>
    </Card>

    <Card>
      <div
        class="w-12 h-12 bg-silver/20 rounded-full flex items-center justify-center mb-6 text-2xl"
      >
        ☁️
      </div>
      <h3 class="text-2xl text-text font-display mb-4">Cloud Geometry</h3>
      <p class="text-text/70 mb-6 leading-relaxed">
        Architecting crystalline structures in the cloud that are both beautiful
        and unbreakable.
      </p>
      <div class="text-silver text-xs font-bold uppercase tracking-widest">
        AWS • Terraform
      </div>
    </Card>
  </div>

  <div class="text-center mt-16">
    <Button href="/services" variant="ghost">Explore All Arts &rarr;</Button>
  </div>
</Section>

<!-- CTA -->
<Section class="text-center">
  <div
    class="max-w-4xl mx-auto bg-white/60 backdrop-blur-xl border border-white/80 rounded-3xl p-16 shadow-xl relative overflow-hidden"
  >
    <div
      class="absolute -top-24 -right-24 w-64 h-64 bg-emerald/20 rounded-full blur-3xl"
    ></div>

    <h2 class="text-4xl md:text-5xl text-text mb-8 font-display">
      Ready to Ascend?
    </h2>
    <p class="text-text/70 mb-10 text-lg max-w-2xl mx-auto">
      Let us weave the spells that will elevate your infrastructure to a higher
      plane of existence.
    </p>
    <Button href="/contact" variant="primary">Initiate Contact</Button>
  </div>
</Section>
