<script lang="ts">
    import { page } from "$app/stores";
    import WorkshopSection from "$lib/components/WorkshopSection.svelte";
    import TileBand from "$lib/components/TileBand.svelte";

    const slug = $page.params.slug;
</script>

<svelte:head>
    <title>Insight: {slug} | Digital Sorcery</title>
</svelte:head>

<div class="bg-andalus-night pt-24 pb-12 text-center">
    <div class="max-w-4xl mx-auto px-4">
        <div
            class="inline-flex items-center gap-2 text-caliphate-gold text-sm font-medium mb-4"
        >
            <span>October 12, 1024</span>
            <span>•</span>
            <span>Platform Engineering</span>
        </div>
        <h1
            class="font-display font-bold text-4xl md:text-5xl text-moonlight-ivory mb-6 capitalize"
        >
            {slug.replace(/-/g, " ")}
        </h1>
    </div>
</div>

<TileBand />

<WorkshopSection variant="light">
    <div class="max-w-3xl mx-auto prose prose-lg prose-stone">
        <p class="lead text-xl text-ink-charcoal font-medium">
            This is a placeholder for the blog post content. In a production
            environment, this would be populated from a CMS or markdown file.
        </p>

        <p>
            Platform engineering is more than just tools; it's about culture.
            It's about creating a paved road for developers to ship code safely
            and quickly.
        </p>

        <h2>The Three Pillars</h2>
        <p>We believe in three core pillars of platform engineering:</p>
        <ol>
            <li>
                <strong>Self-Service:</strong> Developers should be able to provision
                resources without waiting for a ticket.
            </li>
            <li>
                <strong>Automation:</strong> Everything that can be automated, should
                be.
            </li>
            <li>
                <strong>Observability:</strong> You can't fix what you can't see.
            </li>
        </ol>

        <blockquote>
            "The best platform is the one you don't notice."
        </blockquote>
    </div>
</WorkshopSection>
