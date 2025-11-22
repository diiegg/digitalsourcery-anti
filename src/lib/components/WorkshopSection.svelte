<script lang="ts">
    import { clsx } from "clsx";
    import { twMerge } from "tailwind-merge";

    type Variant = "light" | "dark" | "parchment";

    let {
        children,
        variant = "light",
        id = "",
        class: className = "",
    } = $props();

    const variants: Record<Variant, string> = {
        light: "bg-courtyard-plaster text-ink-charcoal",
        dark: "bg-andalus-night text-moonlight-ivory",
        parchment: "bg-parchment-page text-ink-charcoal",
    };
</script>

<section
    {id}
    class={twMerge(
        "py-16 md:py-24 relative overflow-hidden transition-colors duration-500",
        variants[variant as Variant],
        className,
    )}
>
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
        {@render children()}
    </div>

    <!-- Subtle grain or pattern overlay could go here -->
</section>
