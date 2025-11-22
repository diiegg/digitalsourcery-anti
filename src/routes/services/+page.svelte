<script lang="ts">
    import WorkshopSection from "$lib/components/WorkshopSection.svelte";
    import ArchCard from "$lib/components/ArchCard.svelte";
    import TileBand from "$lib/components/TileBand.svelte";
</script>

<svelte:head>
    <title>Rituals & Workings | Digital Sorcery</title>
    <meta
        name="description"
        content="Our services: Platform Engineering, CI/CD Automation, SRE, and Governance."
    />
</svelte:head>

<div class="bg-andalus-night pt-24 pb-12 text-center">
    <div class="max-w-4xl mx-auto px-4">
        <h1
            class="font-display font-bold text-4xl md:text-5xl text-moonlight-ivory mb-6"
        >
            Rituals & Workings
        </h1>
        <p class="text-stone-column text-xl leading-relaxed">
            We offer a suite of specialized services to elevate your platform's
            resilience, velocity, and security.
        </p>
    </div>
</div>

<TileBand />

<WorkshopSection variant="light">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
        <div class="space-y-6">
            <h2 class="font-display font-bold text-3xl text-ink-charcoal">
                Platform Engineering
            </h2>
            <p class="text-stone-column/80 leading-relaxed">
                We build Internal Developer Platforms (IDP) that treat your
                developers as customers. By abstracting complexity and providing
                self-service capabilities, we unlock velocity without
                sacrificing control.
            </p>
            <ul class="space-y-3">
                {#each ["Kubernetes Architecture", "Crossplane & Terraform", "Backstage Implementation", "GitOps Workflows"] as item}
                    <li class="flex items-center gap-3 text-ink-charcoal">
                        <span class="w-1.5 h-1.5 rounded-full bg-caliphate-gold"
                        ></span>
                        {item}
                    </li>
                {/each}
            </ul>
        </div>
        <div
            class="bg-parchment-page rounded-lg p-8 border border-stone-column/20"
        >
            <!-- Placeholder for diagram/image -->
            <div
                class="aspect-video bg-stone-column/10 rounded flex items-center justify-center text-stone-column/50"
            >
                Platform Architecture Diagram
            </div>
        </div>
    </div>
</WorkshopSection>

<WorkshopSection variant="parchment">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12 md:flex-row-reverse">
        <div class="md:order-2 space-y-6">
            <h2 class="font-display font-bold text-3xl text-ink-charcoal">
                CI/CD Automation
            </h2>
            <p class="text-stone-column/80 leading-relaxed">
                From code commit to production deployment, we forge unbreakable
                pipelines. We automate testing, security scanning, and
                deployment strategies to ensure safety at speed.
            </p>
            <ul class="space-y-3">
                {#each ["GitHub Actions & GitLab CI", "ArgoCD & Flux", "Container Security", "Release Engineering"] as item}
                    <li class="flex items-center gap-3 text-ink-charcoal">
                        <span class="w-1.5 h-1.5 rounded-full bg-caliphate-gold"
                        ></span>
                        {item}
                    </li>
                {/each}
            </ul>
        </div>
        <div
            class="md:order-1 bg-white/50 rounded-lg p-8 border border-stone-column/20"
        >
            <!-- Placeholder for diagram/image -->
            <div
                class="aspect-video bg-stone-column/10 rounded flex items-center justify-center text-stone-column/50"
            >
                Pipeline Visualization
            </div>
        </div>
    </div>
</WorkshopSection>

<WorkshopSection variant="light">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
        <div class="space-y-6">
            <h2 class="font-display font-bold text-3xl text-ink-charcoal">
                SRE & Reliability
            </h2>
            <p class="text-stone-column/80 leading-relaxed">
                We bring order to chaos. Through advanced observability, chaos
                engineering, and incident response planning, we ensure your
                systems can withstand the unexpected.
            </p>
            <ul class="space-y-3">
                {#each ["OpenTelemetry & Prometheus", "SLO/SLI Definition", "Chaos Engineering", "Incident Response Playbooks"] as item}
                    <li class="flex items-center gap-3 text-ink-charcoal">
                        <span class="w-1.5 h-1.5 rounded-full bg-caliphate-gold"
                        ></span>
                        {item}
                    </li>
                {/each}
            </ul>
        </div>
        <div
            class="bg-parchment-page rounded-lg p-8 border border-stone-column/20"
        >
            <!-- Placeholder for diagram/image -->
            <div
                class="aspect-video bg-stone-column/10 rounded flex items-center justify-center text-stone-column/50"
            >
                Reliability Metrics
            </div>
        </div>
    </div>
</WorkshopSection>

<WorkshopSection variant="dark" class="text-center">
    <h2 class="font-display font-bold text-3xl text-moonlight-ivory mb-6">
        Ready to Begin?
    </h2>
    <a
        href="/contact"
        class="inline-block bg-mezquita-red text-moonlight-ivory px-8 py-4 rounded-lg font-bold hover:bg-red-700 transition-all shadow-lg shadow-mezquita-red/20"
    >
        Summon the Circle
    </a>
</WorkshopSection>
