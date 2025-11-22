<script lang="ts">
    import { type Snippet } from "svelte";

    type Props = {
        variant?: "primary" | "secondary" | "ghost";
        href?: string;
        type?: "button" | "submit" | "reset";
        class?: string;
        children: Snippet;
        onclick?: () => void;
    };

    let {
        variant = "primary",
        href,
        type = "button",
        class: className = "",
        children,
        onclick,
    }: Props = $props();

    const baseStyles =
        "relative inline-flex items-center justify-center px-8 py-3 text-sm font-bold tracking-wide transition-all duration-300 rounded-full focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-sandstone font-display overflow-hidden group";

    const variants = {
        primary:
            "bg-emerald text-white hover:bg-emerald/90 hover:shadow-[0_10px_20px_-5px_rgba(16,185,129,0.4)] hover:-translate-y-0.5",
        secondary:
            "bg-white border border-silver/30 text-text hover:border-energy/50 hover:text-energy hover:shadow-[0_10px_20px_-5px_rgba(234,88,12,0.2)] hover:-translate-y-0.5",
        ghost: "bg-transparent text-silver hover:text-emerald hover:bg-emerald/5",
    };
</script>

{#if href}
    <a {href} class="{baseStyles} {variants[variant]} {className}" {onclick}>
        <span class="relative z-10">{@render children()}</span>
        {#if variant === "primary"}
            <div
                class="absolute inset-0 bg-gradient-to-r from-white/0 via-white/20 to-white/0 translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-700"
            ></div>
        {/if}
    </a>
{:else}
    <button
        {type}
        class="{baseStyles} {variants[variant]} {className}"
        {onclick}
    >
        <span class="relative z-10">{@render children()}</span>
        {#if variant === "primary"}
            <div
                class="absolute inset-0 bg-gradient-to-r from-white/0 via-white/20 to-white/0 translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-700"
            ></div>
        {/if}
    </button>
{/if}
