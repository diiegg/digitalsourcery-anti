<script lang="ts">
    import ScriptoriumList from "$lib/components/ScriptoriumList.svelte";
    import TileBand from "$lib/components/TileBand.svelte";
</script>

<svelte:head>
    <title>Scriptorium (Insights) | Digital Sorcery</title>
    <meta
        name="description"
        content="Thoughts, guides, and incantations on platform engineering."
    />
</svelte:head>

<div class="bg-andalus-night pt-24 pb-12 text-center">
    <div class="max-w-4xl mx-auto px-4">
        <h1
            class="font-display font-bold text-4xl md:text-5xl text-moonlight-ivory mb-6"
        >
            The Scriptorium
        </h1>
        <p class="text-stone-column text-xl leading-relaxed">
            Knowledge is the only resource that grows when shared. Explore our
            library of insights.
        </p>
    </div>
</div>

<TileBand />

<ScriptoriumList />
