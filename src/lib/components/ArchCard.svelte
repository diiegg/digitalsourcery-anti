<script lang="ts">
    import { twMerge } from "tailwind-merge";

    let {
        title,
        description,
        href = undefined,
        icon = undefined,
        class: className = "",
    } = $props();

    const BaseTag = href ? "a" : "div";
</script>

<svelte:element
    this={BaseTag}
    {href}
    class={twMerge(
        "group relative flex flex-col p-8 rounded-t-[4rem] rounded-b-lg border border-stone-column/20 bg-white/50 backdrop-blur-sm hover:bg-white/80 transition-all duration-300 hover:shadow-xl hover:shadow-caliphate-gold/10 hover:-translate-y-1",
        className,
    )}
>
    {#if icon}
        <div
            class="mb-6 text-caliphate-gold group-hover:text-mezquita-red transition-colors duration-300"
        >
            {@render icon()}
        </div>
    {/if}

    <h3
        class="font-display font-bold text-xl mb-3 text-ink-charcoal group-hover:text-mezquita-red transition-colors"
    >
        {title}
    </h3>

    <p class="text-stone-column/80 text-sm leading-relaxed flex-grow">
        {description}
    </p>

    {#if href}
        <div
            class="mt-6 text-sm font-semibold text-tile-lapis flex items-center gap-2 group-hover:gap-3 transition-all"
        >
            <span>Explore</span>
            <span aria-hidden="true">&rarr;</span>
        </div>
    {/if}
</svelte:element>
