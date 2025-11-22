<script lang="ts">
    import WorkshopSection from "./WorkshopSection.svelte";

    const steps = [
        {
            title: "Discovery",
            description:
                "We map the celestial bodies of your current infrastructure, identifying bottlenecks and alignment issues.",
            icon: "Observation",
        },
        {
            title: "Design",
            description:
                "Drafting the blueprints. We select the right rituals (tools) and incantations (configurations) for your needs.",
            icon: "Blueprint",
        },
        {
            title: "Implementation",
            description:
                "The transmutation begins. We build, automate, and deploy your new platform foundations.",
            icon: "Transmutation",
        },
        {
            title: "Stewardship",
            description:
                "Ongoing observation and tuning. We ensure the magic remains stable and potent as you scale.",
            icon: "Stewardship",
        },
    ];
</script>

<WorkshopSection variant="parchment" id="approach">
    <div class="text-center max-w-3xl mx-auto mb-16">
        <h2
            class="font-display font-bold text-3xl md:text-4xl mb-4 text-ink-charcoal"
        >
            The Grimoire
        </h2>
        <p class="text-stone-column/80 text-lg">
            Our methodology is a cycle of observation, design, and refinement.
        </p>
    </div>

    <div class="relative">
        <!-- Vertical line -->
        <div
            class="absolute left-4 md:left-1/2 top-0 bottom-0 w-0.5 bg-stone-column/30 -translate-x-1/2 hidden md:block"
        ></div>
        <div
            class="absolute left-4 top-0 bottom-0 w-0.5 bg-stone-column/30 -translate-x-1/2 md:hidden"
        ></div>

        <div class="space-y-12">
            {#each steps as step, i}
                <div
                    class="relative flex flex-col md:flex-row gap-8 items-start md:items-center group"
                >
                    <!-- Dot -->
                    <div
                        class="absolute left-4 md:left-1/2 -translate-x-1/2 w-4 h-4 rounded-full bg-caliphate-gold border-4 border-parchment-page z-10 group-hover:scale-125 transition-transform"
                    ></div>

                    <!-- Content -->
                    <div
                        class="ml-12 md:ml-0 md:w-1/2 {i % 2 === 0
                            ? 'md:pr-16 md:text-right'
                            : 'md:pl-16 md:order-last'}"
                    >
                        <div
                            class="bg-white/60 backdrop-blur-sm p-6 rounded-lg border border-stone-column/20 shadow-sm hover:shadow-md transition-shadow"
                        >
                            <h3
                                class="font-display font-bold text-xl text-ink-charcoal mb-2"
                            >
                                {step.title}
                            </h3>
                            <p
                                class="text-stone-column/80 text-sm leading-relaxed"
                            >
                                {step.description}
                            </p>
                        </div>
                    </div>

                    <!-- Spacer for the other side -->
                    <div class="hidden md:block md:w-1/2"></div>
                </div>
            {/each}
        </div>
    </div>
</WorkshopSection>
