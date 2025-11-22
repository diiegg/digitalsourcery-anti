<script lang="ts">
    import SummonForm from "$lib/components/SummonForm.svelte";
    import TileBand from "$lib/components/TileBand.svelte";
</script>

<svelte:head>
    <title>Summon the Circle (Contact) | Digital Sorcery</title>
    <meta
        name="description"
        content="Get in touch with us to discuss your platform engineering needs."
    />
</svelte:head>

<div class="bg-andalus-night pt-24 pb-12 text-center">
    <div class="max-w-4xl mx-auto px-4">
        <h1
            class="font-display font-bold text-4xl md:text-5xl text-moonlight-ivory mb-6"
        >
            Summon the Circle
        </h1>
        <p class="text-stone-column text-xl leading-relaxed">
            We are ready to assist you in your journey.
        </p>
    </div>
</div>

<TileBand />

<SummonForm />
