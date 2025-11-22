<script lang="ts">
    import GrimoireTimeline from "$lib/components/GrimoireTimeline.svelte";
    import WorkshopSection from "$lib/components/WorkshopSection.svelte";
    import TileBand from "$lib/components/TileBand.svelte";
</script>

<svelte:head>
    <title>The Grimoire (Approach) | Digital Sorcery</title>
    <meta
        name="description"
        content="Our methodology: Discovery, Design, Implementation, and Stewardship."
    />
</svelte:head>

<div class="bg-andalus-night pt-24 pb-12 text-center">
    <div class="max-w-4xl mx-auto px-4">
        <h1
            class="font-display font-bold text-4xl md:text-5xl text-moonlight-ivory mb-6"
        >
            The Grimoire
        </h1>
        <p class="text-stone-column text-xl leading-relaxed">
            Our methodology is a cycle of observation, design, and refinement.
            We do not simply build; we cultivate.
        </p>
    </div>
</div>

<TileBand />

<GrimoireTimeline />

<WorkshopSection variant="light">
    <div class="max-w-3xl mx-auto text-center">
        <h2 class="font-display font-bold text-3xl text-ink-charcoal mb-6">
            Philosophy
        </h2>
        <p class="text-stone-column/80 text-lg leading-relaxed mb-8">
            We believe that platform engineering is an art form. It requires the
            precision of a mathematician and the creativity of an architect. Our
            approach is rooted in the principles of durability, observability,
            and simplicity.
        </p>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-left">
            <div class="p-6 bg-white rounded-lg border border-stone-column/20">
                <h3 class="font-bold text-ink-charcoal mb-2">Durability</h3>
                <p class="text-sm text-stone-column">
                    Systems that stand the test of time and traffic spikes.
                </p>
            </div>
            <div class="p-6 bg-white rounded-lg border border-stone-column/20">
                <h3 class="font-bold text-ink-charcoal mb-2">Observability</h3>
                <p class="text-sm text-stone-column">
                    Seeing the unseen to prevent failures before they happen.
                </p>
            </div>
            <div class="p-6 bg-white rounded-lg border border-stone-column/20">
                <h3 class="font-bold text-ink-charcoal mb-2">Simplicity</h3>
                <p class="text-sm text-stone-column">
                    Complexity is the enemy. We strive for elegant solutions.
                </p>
            </div>
        </div>
    </div>
</WorkshopSection>
