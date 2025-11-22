<script lang="ts">
    import ArchCard from "./ArchCard.svelte";
    import WorkshopSection from "./WorkshopSection.svelte";

    // Icons would ideally be imported from a library like lucide-svelte,
    // but for now we'll use simple SVG placeholders or text in the ArchCard slots if needed.
    // Or we can pass a snippet.
</script>

<WorkshopSection variant="light" id="services">
    <div class="text-center max-w-3xl mx-auto mb-16">
        <h2
            class="font-display font-bold text-3xl md:text-4xl mb-4 text-ink-charcoal"
        >
            Rituals & Workings
        </h2>
        <p class="text-stone-column text-lg">
            Our craft is rooted in precision and foresight. We offer specialized
            services to elevate your platform's resilience and velocity.
        </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <ArchCard
            title="Platform Engineering"
            description="Building the internal developer platforms (IDP) that empower your teams to ship faster with confidence. Kubernetes, ArgoCD, and Crossplane mastery."
            href="/services/platform-engineering"
        >
            {#snippet icon()}
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    class="w-8 h-8"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M21 7.5l-9-5.25L3 7.5m18 0l-9 5.25m9-5.25v9l-9 5.25M3 7.5l9 5.25M3 7.5v9l9 5.25m0-9v9"
                    />
                </svg>
            {/snippet}
        </ArchCard>

        <ArchCard
            title="CI/CD Automation"
            description="Forging unbreakable pipelines. We automate the path from code to production, ensuring safety and speed at every step."
            href="/services/cicd"
        >
            {#snippet icon()}
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    class="w-8 h-8"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M4.5 12a7.5 7.5 0 0015 0m-15 0a7.5 7.5 0 1115 0m-15 0H3m16.5 0H21m-1.5 0H12m-8.457 3.077l1.41-.513m14.095-5.13l1.41-.513M5.106 17.785l1.15-.964m11.49-9.642l1.149-.964M7.501 19.795l.75-1.3m7.5-12.99l.75-1.3m-6.063 16.658l.26-1.477m2.605-14.772l.26-1.477m0 17.726l-.26-1.477M10.698 4.614l-.26-1.477M16.5 19.795l-.75-1.3m-7.5-12.99l-.75-1.3m15.857 11.164l-1.15-.964M5.106 7.178l-1.15-.964m2.553 13.518l-1.41-.513M19.543 4.614l-1.41-.513"
                    />
                </svg>
            {/snippet}
        </ArchCard>

        <ArchCard
            title="SRE & Reliability"
            description="Observability, incident response, and chaos engineering. We ensure your systems stand firm against the entropy of the digital void."
            href="/services/sre"
        >
            {#snippet icon()}
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    class="w-8 h-8"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M3.75 13.5l10.5-11.25L12 10.5h8.25L9.75 21.75 12 13.5H3.75z"
                    />
                </svg>
            {/snippet}
        </ArchCard>
    </div>
</WorkshopSection>
