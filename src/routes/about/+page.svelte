<script lang="ts">
    import WorkshopSection from "$lib/components/WorkshopSection.svelte";
    import TileBand from "$lib/components/TileBand.svelte";
</script>

<svelte:head>
    <title>The Circle (About) | Digital Sorcery</title>
    <meta name="description" content="Who we are and what we stand for." />
</svelte:head>

<div class="bg-andalus-night pt-24 pb-12 text-center">
    <div class="max-w-4xl mx-auto px-4">
        <h1
            class="font-display font-bold text-4xl md:text-5xl text-moonlight-ivory mb-6"
        >
            The Circle
        </h1>
        <p class="text-stone-column text-xl leading-relaxed">
            We are a collective of engineers, architects, and automation experts
            dedicated to the craft of platform building.
        </p>
    </div>
</div>

<TileBand />

<WorkshopSection variant="light">
    <div class="max-w-3xl mx-auto space-y-12">
        <div>
            <h2 class="font-display font-bold text-3xl text-ink-charcoal mb-4">
                Our Origin
            </h2>
            <p class="text-stone-column/80 text-lg leading-relaxed">
                Digital Sorcery was founded on the belief that modern
                infrastructure has become too complex. We looked to the
                past—specifically the Golden Age of al-Andalus—for inspiration.
                In that era, scholars, astronomers, and engineers worked
                together to build systems of lasting beauty and utility. We
                apply that same interdisciplinary approach to cloud native
                technology.
            </p>
        </div>

        <div>
            <h2 class="font-display font-bold text-3xl text-ink-charcoal mb-4">
                Our Values
            </h2>
            <ul class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <li
                    class="bg-parchment-page p-6 rounded-lg border border-stone-column/20"
                >
                    <h3 class="font-bold text-ink-charcoal mb-2">
                        Craftsmanship
                    </h3>
                    <p class="text-sm text-stone-column/80">
                        We take pride in our code and our configurations.
                    </p>
                </li>
                <li
                    class="bg-parchment-page p-6 rounded-lg border border-stone-column/20"
                >
                    <h3 class="font-bold text-ink-charcoal mb-2">
                        Transparency
                    </h3>
                    <p class="text-sm text-stone-column/80">
                        We work in the open. No black boxes.
                    </p>
                </li>
                <li
                    class="bg-parchment-page p-6 rounded-lg border border-stone-column/20"
                >
                    <h3 class="font-bold text-ink-charcoal mb-2">Empathy</h3>
                    <p class="text-sm text-stone-column/80">
                        We build for humans, not just machines.
                    </p>
                </li>
                <li
                    class="bg-parchment-page p-6 rounded-lg border border-stone-column/20"
                >
                    <h3 class="font-bold text-ink-charcoal mb-2">Resilience</h3>
                    <p class="text-sm text-stone-column/80">
                        We design for failure because failure is inevitable.
                    </p>
                </li>
            </ul>
        </div>
    </div>
</WorkshopSection>
