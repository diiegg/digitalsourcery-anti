<script lang="ts">
    import SpellbookList from "$lib/components/SpellbookList.svelte";
    import TileBand from "$lib/components/TileBand.svelte";
</script>

<svelte:head>
    <title>Spellbook (Case Studies) | Digital Sorcery</title>
    <meta
        name="description"
        content="Case studies and success stories from our engagements."
    />
</svelte:head>

<div class="bg-andalus-night pt-24 pb-12 text-center">
    <div class="max-w-4xl mx-auto px-4">
        <h1
            class="font-display font-bold text-4xl md:text-5xl text-moonlight-ivory mb-6"
        >
            The Spellbook
        </h1>
        <p class="text-stone-column text-xl leading-relaxed">
            A chronicle of our transmutations. See how we've helped
            organizations evolve their infrastructure.
        </p>
    </div>
</div>

<TileBand />

<SpellbookList />
