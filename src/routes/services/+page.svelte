<script lang="ts">
    import Button from "$lib/components/Button.svelte";
    import Card from "$lib/components/Card.svelte";
    import Section from "$lib/components/Section.svelte";

    const services = [
        {
            title: "Platform Ecology",
            description:
                "We build Internal Developer Platforms (IDP) that treat your developers as gardeners of code. Reduce cognitive load and accelerate growth.",
            tech: ["Kubernetes", "Backstage", "Crossplane", "Port"],
            icon: "🌱",
        },
        {
            title: "Automated Flow",
            description:
                "From CI/CD pipelines to GitOps workflows, we automate the toil away. Your deployments should be as natural as the tides.",
            tech: ["GitHub Actions", "GitLab CI", "ArgoCD", "Flux"],
            icon: "🌊",
        },
        {
            title: "Cloud Geometry",
            description:
                "Designing scalable, secure, and cost-effective cloud environments. We treat infrastructure as sacred geometry.",
            tech: ["AWS", "GCP", "Azure", "Terraform", "OpenTofu"],
            icon: "✨",
        },
        {
            title: "Crystal Wards",
            description:
                "DevSecOps integration to protect your digital assets. Automated scanning, policy enforcement, and compliance as code.",
            tech: ["Snyk", "Trivy", "OPA", "Kyverno"],
            icon: "🛡️",
        },
        {
            title: "Clairvoyance",
            description:
                "Gaze into the system and understand its behavior. Full-stack monitoring, logging, and tracing implementation.",
            tech: ["Prometheus", "Grafana", "OpenTelemetry", "Datadog"],
            icon: "👁️",
        },
        {
            title: "Legacy Transmutation",
            description:
                "Modernizing monolithic applications into microservices. We guide you through the transformation process.",
            tech: ["Docker", "Serverless", "Migration Strategies"],
            icon: "⚗️",
        },
    ];
</script>

<svelte:head>
    <title>Services | Digital Sorcery</title>
</svelte:head>

<Section class="pt-32 pb-10 text-center">
    <h1 class="text-6xl md:text-8xl text-text mb-8 font-display tracking-tight">
        The Grimoire
    </h1>
    <p class="text-xl text-silver max-w-2xl mx-auto font-light">
        Our catalog of elemental services designed to harmonize your technology.
    </p>
</Section>

<Section>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
        {#each services as service}
            <Card class="h-full">
                <div class="flex items-start justify-between mb-6">
                    <h3 class="text-3xl text-text font-display">
                        {service.title}
                    </h3>
                    <span class="text-5xl opacity-80">{service.icon}</span>
                </div>
                <p
                    class="text-text/70 mb-8 leading-relaxed min-h-[80px] text-lg"
                >
                    {service.description}
                </p>
                <div class="border-t border-silver/20 pt-6">
                    <div
                        class="text-xs text-emerald font-bold uppercase tracking-widest mb-3"
                    >
                        Technologies
                    </div>
                    <div class="flex flex-wrap gap-2">
                        {#each service.tech as tech}
                            <span
                                class="px-3 py-1 bg-emerald/10 text-emerald text-xs font-medium rounded-full border border-emerald/20"
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
    <h2 class="text-4xl text-text mb-8 font-display">Need a Custom Ritual?</h2>
    <Button href="/contact" variant="primary">Consult the Oracles</Button>
</Section>
