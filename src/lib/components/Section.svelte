<script lang="ts">
    import { type Snippet } from "svelte";

    type Props = {
        id?: string;
        class?: string;
        children: Snippet;
    };

    let { id, class: className = "", children }: Props = $props();
</script>

<section {id} class="relative py-20 md:py-32 overflow-hidden {className}">
    <div class="container mx-auto px-4 relative z-10">
        {@render children()}
    </div>
</section>
