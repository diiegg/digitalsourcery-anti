<script lang="ts">
    import { type Snippet } from "svelte";

    type Props = {
        id?: string;
        class?: string;
        children: Snippet;
    };

    let { id, class: className = "", children }: Props = $props();
</script>

<section {id} class="relative py-24 md:py-36 overflow-hidden {className}">
    <!-- Background decoration -->
    <div class="absolute inset-0 pointer-events-none opacity-30">
        <div
            class="absolute top-0 left-0 w-full h-px bg-gradient-to-r from-transparent via-silver/20 to-transparent"
        ></div>
    </div>

    <div class="container mx-auto px-4 relative z-10">
        {@render children()}
    </div>
</section>
