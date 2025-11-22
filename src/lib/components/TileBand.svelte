<script lang="ts">
    import { twMerge } from "tailwind-merge";

    let { class: className = "" } = $props();
</script>

<div
    class={twMerge("h-4 w-full bg-repeat-x opacity-30", className)}
    style="background-image: linear-gradient(90deg, var(--color-caliphate-gold) 50%, transparent 50%); background-size: 16px 4px;"
    aria-hidden="true"
></div>
