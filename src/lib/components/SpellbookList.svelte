<script lang="ts">
    import ArchCard from "./ArchCard.svelte";
    import WorkshopSection from "./WorkshopSection.svelte";

    // This would typically come from a prop or data store
    const caseStudies = [
        {
            title: "The Fintech Alchemist",
            description:
                "Migrating a legacy banking core to a cloud-native Kubernetes platform with zero downtime.",
            slug: "fintech-alchemist",
        },
        {
            title: "Automating the Bazaar",
            description:
                "Scaling a global e-commerce marketplace using GitOps and ephemeral environments.",
            slug: "automating-bazaar",
        },
        {
            title: "Guardian of the Vault",
            description:
                "Implementing zero-trust security and compliance automation for a healthcare data provider.",
            slug: "guardian-vault",
        },
    ];
</script>

<WorkshopSection variant="light" id="case-studies">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        {#each caseStudies as study}
            <ArchCard
                title={study.title}
                description={study.description}
                href={`/case-studies/${study.slug}`}
                class="bg-parchment-page/50"
            />
        {/each}
    </div>
</WorkshopSection>
