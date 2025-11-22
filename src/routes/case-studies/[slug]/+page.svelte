<script lang="ts">
    import { page } from "$app/stores";
    import WorkshopSection from "$lib/components/WorkshopSection.svelte";
    import TileBand from "$lib/components/TileBand.svelte";

    // In a real app, we'd fetch data based on $page.params.slug
    const slug = $page.params.slug;
</script>

<svelte:head>
    <title>Case Study: {slug} | Digital Sorcery</title>
</svelte:head>

<div class="bg-andalus-night pt-24 pb-12 text-center">
    <div class="max-w-4xl mx-auto px-4">
        <div
            class="inline-block px-3 py-1 mb-4 rounded-full border border-caliphate-gold/30 bg-caliphate-gold/10 text-caliphate-gold text-sm font-medium"
        >
            Case Study
        </div>
        <h1
            class="font-display font-bold text-4xl md:text-5xl text-moonlight-ivory mb-6 capitalize"
        >
            {slug.replace(/-/g, " ")}
        </h1>
    </div>
</div>

<TileBand />

<WorkshopSection variant="parchment">
    <div class="max-w-3xl mx-auto prose prose-lg prose-stone">
        <p class="lead text-xl text-ink-charcoal font-medium">
            This is a placeholder for the case study content. In a production
            environment, this would be populated from a CMS or markdown file.
        </p>

        <h3>The Challenge</h3>
        <p>
            The client was facing significant technical debt and scalability
            issues...
        </p>

        <h3>The Ritual</h3>
        <p>
            We implemented a GitOps-based workflow using ArgoCD and
            Crossplane...
        </p>

        <h3>The Outcome</h3>
        <ul>
            <li>99.99% Uptime achieved</li>
            <li>Deployment frequency increased by 400%</li>
            <li>Mean Time To Recovery (MTTR) reduced by 80%</li>
        </ul>
    </div>
</WorkshopSection>
