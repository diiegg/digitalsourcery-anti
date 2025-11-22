<script lang="ts">
    import Button from "$lib/components/Button.svelte";
    import Card from "$lib/components/Card.svelte";
    import Section from "$lib/components/Section.svelte";

    const services = [
        {
            title: "Platform Engineering",
            description:
                "We build Internal Developer Platforms (IDP) that treat your developers as customers. Reduce cognitive load and accelerate delivery.",
            tech: ["Kubernetes", "Backstage", "Crossplane", "Port"],
            icon: "⚡",
        },
        {
            title: "Automation Sorcery",
            description:
                "From CI/CD pipelines to GitOps workflows, we automate the toil away. Your deployments should be boring, reliable, and fast.",
            tech: ["GitHub Actions", "GitLab CI", "ArgoCD", "Flux"],
            icon: "🔮",
        },
        {
            title: "Cloud Architecture",
            description:
                "Designing scalable, secure, and cost-effective cloud environments. We treat infrastructure as code, ensuring reproducibility and disaster recovery.",
            tech: ["AWS", "GCP", "Azure", "Terraform", "OpenTofu"],
            icon: "☁️",
        },
        {
            title: "Security Wards",
            description:
                "DevSecOps integration to protect your digital assets. Automated scanning, policy enforcement, and compliance as code.",
            tech: ["Snyk", "Trivy", "OPA", "Kyverno"],
            icon: "🛡️",
        },
        {
            title: "Observability",
            description:
                "Gaze into the void and understand your system's behavior. Full-stack monitoring, logging, and tracing implementation.",
            tech: ["Prometheus", "Grafana", "OpenTelemetry", "Datadog"],
            icon: "👁️",
        },
        {
            title: "Legacy Transmutation",
            description:
                "Modernizing monolithic applications into microservices or serverless architectures. We guide you through the dangerous path of refactoring.",
            tech: ["Docker", "Serverless", "Migration Strategies"],
            icon: "⚗️",
        },
    ];
</script>

<svelte:head>
    <title>Services | Digital Sorcery</title>
</svelte:head>

<Section class="pt-32 pb-10 text-center">
    <h1 class="text-5xl md:text-6xl text-white mb-6">The Grimoire</h1>
    <p class="text-xl text-gray-400 max-w-2xl mx-auto">
        Our catalog of arcane services designed to elevate your technological
        capabilities.
    </p>
</Section>

<Section>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        {#each services as service}
            <Card class="h-full">
                <div class="flex items-start justify-between mb-4">
                    <h3 class="text-2xl text-gold">{service.title}</h3>
                    <span class="text-4xl">{service.icon}</span>
                </div>
                <p class="text-gray-400 mb-6 leading-relaxed min-h-[80px]">
                    {service.description}
                </p>
                <div class="border-t border-white/10 pt-4">
                    <div
                        class="text-xs text-mana uppercase tracking-wider mb-2"
                    >
                        Technologies
                    </div>
                    <div class="flex flex-wrap gap-2">
                        {#each service.tech as tech}
                            <span
                                class="px-2 py-1 bg-mana/10 text-mana text-xs rounded border border-mana/20"
                            >
                                {tech}
                            </span>
                        {/each}
                    </div>
                </div>
            </Card>
        {/each}
    </div>
</Section>

<Section class="text-center">
    <h2 class="text-3xl text-white mb-8">Need a Custom Spell?</h2>
    <Button href="/contact" variant="primary">Consult the Oracles</Button>
</Section>
