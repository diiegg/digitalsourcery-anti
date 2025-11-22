<script lang="ts">
    import WorkshopSection from "./WorkshopSection.svelte";

    const insights = [
        {
            title: "The Art of Platform Stewardship",
            excerpt:
                "Why platform engineering is more about gardening than construction.",
            date: "October 12, 1024", // Stylized date
            slug: "platform-stewardship",
            tags: ["Philosophy", "Culture"],
        },
        {
            title: "Incantations in YAML",
            excerpt:
                "Managing complexity in Kubernetes manifests without losing your sanity.",
            date: "September 28, 1024",
            slug: "incantations-yaml",
            tags: ["Technical", "Kubernetes"],
        },
        {
            title: "Observing the Celestial Spheres",
            excerpt:
                "A guide to modern observability stacks using OpenTelemetry.",
            date: "September 15, 1024",
            slug: "observing-spheres",
            tags: ["Observability", "Tools"],
        },
    ];
</script>

<WorkshopSection variant="light" id="insights">
    <div class="space-y-8 max-w-4xl mx-auto">
        {#each insights as post}
            <article
                class="group relative bg-white p-8 rounded-lg border border-stone-column/20 hover:border-caliphate-gold transition-colors shadow-sm hover:shadow-md"
            >
                <div
                    class="flex flex-col md:flex-row md:items-baseline gap-2 md:gap-4 mb-2"
                >
                    <h3
                        class="text-2xl font-display font-bold text-ink-charcoal group-hover:text-mezquita-red transition-colors"
                    >
                        <a href={`/insights/${post.slug}`}>
                            <span class="absolute inset-0"></span>
                            {post.title}
                        </a>
                    </h3>
                    <span class="text-sm text-stone-column font-medium"
                        >{post.date}</span
                    >
                </div>

                <p class="text-stone-column/80 mb-4 leading-relaxed">
                    {post.excerpt}
                </p>

                <div class="flex gap-2">
                    {#each post.tags as tag}
                        <span
                            class="text-xs font-semibold px-2 py-1 rounded bg-stone-column/10 text-stone-column"
                        >
                            {tag}
                        </span>
                    {/each}
                </div>
            </article>
        {/each}
    </div>
</WorkshopSection>
