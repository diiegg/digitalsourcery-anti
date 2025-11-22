<script lang="ts">
    import { type Snippet } from "svelte";

    type Props = {
        class?: string;
        children: Snippet;
    };

    let { class: className = "", children }: Props = $props();
</script>

<div class="relative group {className}">
    <!-- Glow effect behind card -->
    <div
        class="absolute -inset-0.5 bg-gradient-to-r from-mana/20 to-arcane/20 rounded-lg blur opacity-0 group-hover:opacity-100 transition duration-500"
    ></div>

    <!-- Card content -->
    <div
        class="relative h-full p-6 bg-void/80 backdrop-blur-sm border border-white/10 rounded-lg hover:border-mana/30 transition-colors duration-300"
    >
        {@render children()}
    </div>
</div>
