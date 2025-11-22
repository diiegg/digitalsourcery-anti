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
        "relative inline-flex items-center justify-center px-6 py-3 text-sm font-bold tracking-wider uppercase transition-all duration-300 rounded-sm focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-void font-display";

    const variants = {
        primary:
            "bg-mana text-void hover:bg-white hover:shadow-[0_0_20px_rgba(0,243,255,0.6)] focus:ring-mana",
        secondary:
            "bg-transparent border border-arcane text-arcane hover:bg-arcane/10 hover:shadow-[0_0_15px_rgba(157,0,255,0.4)] focus:ring-arcane",
        ghost: "bg-transparent text-gray-400 hover:text-white hover:bg-white/5 focus:ring-gray-500",
    };
</script>

{#if href}
    <a {href} class="{baseStyles} {variants[variant]} {className}" {onclick}>
        {@render children()}
    </a>
{:else}
    <button
        {type}
        class="{baseStyles} {variants[variant]} {className}"
        {onclick}
    >
        {@render children()}
    </button>
{/if}
