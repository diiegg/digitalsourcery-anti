<script lang="ts">
    type Props = {
        label: string;
        id: string;
        type?: "text" | "email" | "textarea";
        value?: string;
        placeholder?: string;
        required?: boolean;
        rows?: number;
    };

    let {
        label,
        id,
        type = "text",
        value = $bindable(""),
        placeholder = "",
        required = false,
        rows = 4,
    }: Props = $props();
</script>

<div class="group relative z-0 w-full mb-8">
    {#if type === "textarea"}
        <textarea
            {id}
            {rows}
            class="block py-3 px-4 w-full text-sm text-text bg-white/50 border border-silver/30 rounded-lg appearance-none focus:outline-none focus:ring-2 focus:ring-emerald/20 focus:border-emerald transition-all resize-none placeholder-transparent"
            {placeholder}
            {required}
            bind:value
        ></textarea>
    {:else}
        <input
            {type}
            {id}
            class="block py-3 px-4 w-full text-sm text-text bg-white/50 border border-silver/30 rounded-lg appearance-none focus:outline-none focus:ring-2 focus:ring-emerald/20 focus:border-emerald transition-all placeholder-transparent"
            {placeholder}
            {required}
            bind:value
        />
    {/if}
    <label
        for={id}
        class="absolute text-sm text-silver duration-300 transform -translate-y-3 scale-75 top-1 z-10 origin-[0] bg-sandstone px-2 left-3 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-3 peer-placeholder-shown:top-0 peer-focus:scale-75 peer-focus:-translate-y-3 peer-focus:text-emerald"
    >
        {label}
    </label>
</div>
