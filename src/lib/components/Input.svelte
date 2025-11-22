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

<div class="group relative z-0 w-full mb-6">
    {#if type === "textarea"}
        <textarea
            {id}
            {rows}
            class="block py-2.5 px-0 w-full text-sm text-white bg-transparent border-0 border-b-2 border-gray-600 appearance-none focus:outline-none focus:ring-0 focus:border-mana peer resize-none"
            {placeholder}
            {required}
            bind:value
        ></textarea>
    {:else}
        <input
            {type}
            {id}
            class="block py-2.5 px-0 w-full text-sm text-white bg-transparent border-0 border-b-2 border-gray-600 appearance-none focus:outline-none focus:ring-0 focus:border-mana peer"
            {placeholder}
            {required}
            bind:value
        />
    {/if}
    <label
        for={id}
        class="peer-focus:font-medium absolute text-sm text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-focus:text-mana peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
    >
        {label}
    </label>
</div>
