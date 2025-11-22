<script lang="ts">
    import { type Snippet } from "svelte";

    type Props = {
        class?: string;
        children: Snippet;
    };

    let { class: className = "", children }: Props = $props();
</script>

<div class="relative group {className}">
    <!-- Card content -->
    <div
        class="relative h-full p-8 bg-white/40 backdrop-blur-md border border-white/60 rounded-2xl shadow-[0_8px_32px_0_rgba(31,38,135,0.05)] hover:shadow-[0_8px_32px_0_rgba(16,185,129,0.1)] hover:border-emerald/30 transition-all duration-500 hover:-translate-y-1"
    >
        {@render children()}
    </div>

    <!-- Decorative geometric element -->
    <div
        class="absolute -top-2 -right-2 w-12 h-12 bg-gradient-to-br from-emerald/20 to-energy/20 rounded-full blur-xl opacity-0 group-hover:opacity-100 transition duration-500"
    ></div>
</div>
