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
        alert(`Spell cast! We will contact ${formState.email} shortly.`);
    }
</script>

<svelte:head>
    <title>Contact | Digital Sorcery</title>
</svelte:head>

<Section class="pt-32 pb-10 text-center">
    <h1 class="text-5xl md:text-6xl text-white mb-6">Summon Us</h1>
    <p class="text-xl text-gray-400 max-w-2xl mx-auto">
        Ready to transform your infrastructure? Send a signal through the void.
    </p>
</Section>

<Section>
    <div class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-12">
        <!-- Contact Info -->
        <div>
            <h2 class="text-2xl text-white mb-6">Transmission Frequencies</h2>
            <p class="text-gray-400 mb-8">
                Our wizards are constantly monitoring the ether for new
                opportunities. Expect a response within one planetary rotation.
            </p>

            <div class="space-y-6">
                <div class="flex items-center space-x-4">
                    <div
                        class="w-10 h-10 rounded-full bg-mana/10 flex items-center justify-center text-mana"
                    >
                        ✉️
                    </div>
                    <div>
                        <div
                            class="text-sm text-gray-500 uppercase tracking-wider"
                        >
                            Email
                        </div>
                        <a
                            href="mailto:hello@digitalsorcery.dev"
                            class="text-white hover:text-mana transition-colors"
                            >hello@digitalsorcery.dev</a
                        >
                    </div>
                </div>

                <div class="flex items-center space-x-4">
                    <div
                        class="w-10 h-10 rounded-full bg-arcane/10 flex items-center justify-center text-arcane"
                    >
                        📍
                    </div>
                    <div>
                        <div
                            class="text-sm text-gray-500 uppercase tracking-wider"
                        >
                            Base of Operations
                        </div>
                        <div class="text-white">The Cloud (Remote First)</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Contact Form -->
        <div class="bg-white/5 p-8 rounded-2xl border border-white/10">
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

                <div class="mt-8">
                    <Button type="submit" variant="primary" class="w-full">
                        Send Transmission
                    </Button>
                </div>
            </form>
        </div>
    </div>
</Section>
