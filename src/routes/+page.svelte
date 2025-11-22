<script lang="ts">
    import WorkshopHero from "$lib/components/WorkshopHero.svelte";
    import ServiceWorkbenchGrid from "$lib/components/ServiceWorkbenchGrid.svelte";
    import GrimoireTimeline from "$lib/components/GrimoireTimeline.svelte";
    import SummonForm from "$lib/components/SummonForm.svelte";
    import WorkshopSection from "$lib/components/WorkshopSection.svelte";
    import ArchCard from "$lib/components/ArchCard.svelte";
</script>

<svelte:head>
    <title>Digital Sorcery | Platform Engineering & Automation</title>
    <meta
        name="description"
        content="Constructing the observatories of the digital age. Platform engineering, SRE, and automation consulting services."
    />
</svelte:head>

<WorkshopHero />

<ServiceWorkbenchGrid />

<GrimoireTimeline />

<WorkshopSection variant="light" id="latest-work">
    <div class="text-center max-w-3xl mx-auto mb-16">
        <h2
            class="font-display font-bold text-3xl md:text-4xl mb-4 text-ink-charcoal"
        >
            Recent Transmutations
        </h2>
        <p class="text-stone-column text-lg">
            Selected case studies from our spellbook.
        </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <ArchCard
            title="The Fintech Alchemist"
            description="Migrating a legacy banking core to a cloud-native Kubernetes platform with zero downtime."
            href="/case-studies/fintech-alchemist"
            class="bg-white"
        />
        <ArchCard
            title="Automating the Bazaar"
            description="Scaling a global e-commerce marketplace using GitOps and ephemeral environments."
            href="/case-studies/automating-bazaar"
            class="bg-white"
        />
        <ArchCard
            title="Guardian of the Vault"
            description="Implementing zero-trust security and compliance automation for a healthcare data provider."
            href="/case-studies/guardian-vault"
            class="bg-white"
        />
    </div>

    <div class="text-center mt-12">
        <a
            href="/case-studies"
            class="inline-flex items-center gap-2 text-mezquita-red font-bold hover:gap-3 transition-all"
        >
            View All Case Studies <span aria-hidden="true">&rarr;</span>
        </a>
    </div>
</WorkshopSection>

<SummonForm />
