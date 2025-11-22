<script lang="ts">
    import Button from "$lib/components/Button.svelte";
    import Section from "$lib/components/Section.svelte";
    import Input from "$lib/components/Input.svelte";

    let formState = $state({
        name: "",
        email: "",
        company: "",
        message: "",
    });

    function handleSubmit(e: Event) {
        e.preventDefault();
        alert(
            `Transmission received! We will contact ${formState.email} shortly.`,
        );
    }
</script>

<svelte:head>
    <title>Contact | Digital Sorcery</title>
</svelte:head>

<Section class="pt-32 pb-10 text-center">
    <h1 class="text-6xl md:text-8xl text-text mb-8 font-display tracking-tight">
        Summon Us
    </h1>
    <p class="text-xl text-silver max-w-2xl mx-auto font-light">
        Ready to transform your infrastructure? Send a signal through the ether.
    </p>
</Section>

<Section>
    <div class="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-16">
        <!-- Contact Info -->
        <div>
            <h2 class="text-3xl text-text mb-8 font-display">
                Transmission Frequencies
            </h2>
            <p class="text-text/70 mb-10 text-lg leading-relaxed">
                Our alchemists are constantly monitoring the frequencies for new
                opportunities. Expect a response within one solar rotation.
            </p>

            <div class="space-y-8">
                <div class="flex items-center space-x-6 group">
                    <div
                        class="w-14 h-14 rounded-full bg-emerald/10 flex items-center justify-center text-emerald text-2xl group-hover:bg-emerald group-hover:text-white transition-colors duration-300"
                    >
                        ✉️
                    </div>
                    <div>
                        <div
                            class="text-xs text-silver uppercase tracking-widest font-bold mb-1"
                        >
                            Email
                        </div>
                        <a
                            href="mailto:hello@digitalsorcery.dev"
                            class="text-text text-lg hover:text-emerald transition-colors font-display"
                            >hello@digitalsorcery.dev</a
                        >
                    </div>
                </div>

                <div class="flex items-center space-x-6 group">
                    <div
                        class="w-14 h-14 rounded-full bg-energy/10 flex items-center justify-center text-energy text-2xl group-hover:bg-energy group-hover:text-white transition-colors duration-300"
                    >
                        📍
                    </div>
                    <div>
                        <div
                            class="text-xs text-silver uppercase tracking-widest font-bold mb-1"
                        >
                            Base of Operations
                        </div>
                        <div class="text-text text-lg font-display">
                            The Cloud (Remote First)
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Contact Form -->
        <div
            class="bg-white/60 backdrop-blur-xl p-10 rounded-3xl border border-white/80 shadow-lg"
        >
            <form onsubmit={handleSubmit}>
                <Input
                    id="name"
                    label="Your Name"
                    bind:value={formState.name}
                    required
                />
                <Input
                    id="email"
                    label="Email Address"
                    type="email"
                    bind:value={formState.email}
                    required
                />
                <Input
                    id="company"
                    label="Company / Guild"
                    bind:value={formState.company}
                />
                <Input
                    id="message"
                    label="Message / Incantation"
                    type="textarea"
                    bind:value={formState.message}
                    required
                />

                <div class="mt-10">
                    <Button type="submit" variant="primary" class="w-full">
                        Send Transmission
                    </Button>
                </div>
            </form>
        </div>
    </div>
</Section>
