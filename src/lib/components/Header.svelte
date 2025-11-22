<script lang="ts">
    import { page } from "$app/stores";
    import Button from "./Button.svelte";

    let isMenuOpen = $state(false);

    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }

    const links = [
        { href: "/", label: "Home" },
        { href: "/services", label: "Services" },
        { href: "/contact", label: "Contact" },
    ];
</script>

<header
    class="fixed w-full top-0 z-50 bg-white/70 backdrop-blur-lg border-b border-white/40 shadow-sm"
>
    <div class="container mx-auto px-4">
        <div class="flex items-center justify-between h-24">
            <!-- Logo -->
            <a
                href="/"
                class="text-2xl font-display font-bold text-text tracking-tight hover:text-emerald transition-colors flex items-center gap-2"
            >
                <span class="text-emerald text-3xl">✦</span>
                DIGITAL<span class="font-light">SORCERY</span>
            </a>

            <!-- Desktop Nav -->
            <nav class="hidden md:flex items-center space-x-10">
                {#each links as link}
                    <a
                        href={link.href}
                        class="text-sm font-medium uppercase tracking-widest hover:text-emerald transition-colors relative group {$page
                            .url.pathname === link.href
                            ? 'text-emerald'
                            : 'text-silver'}"
                    >
                        {link.label}
                        <span
                            class="absolute -bottom-1 left-0 w-0 h-px bg-emerald transition-all duration-300 group-hover:w-full"
                        ></span>
                    </a>
                {/each}
                <Button
                    href="/contact"
                    variant="primary"
                    class="ml-6 !py-2 !px-6 !text-xs"
                >
                    Summon Us
                </Button>
            </nav>

            <!-- Mobile Menu Button -->
            <button
                class="md:hidden text-text p-2"
                onclick={toggleMenu}
                aria-label="Toggle menu"
            >
                <svg
                    class="w-6 h-6"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                >
                    {#if isMenuOpen}
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M6 18L18 6M6 6l12 12"
                        />
                    {:else}
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M4 6h16M4 12h16M4 18h16"
                        />
                    {/if}
                </svg>
            </button>
        </div>
    </div>

    <!-- Mobile Nav -->
    {#if isMenuOpen}
        <div class="md:hidden bg-sandstone border-b border-white/20">
            <nav class="flex flex-col p-6 space-y-6">
                {#each links as link}
                    <a
                        href={link.href}
                        class="text-lg font-display font-medium tracking-wide hover:text-emerald transition-colors {$page
                            .url.pathname === link.href
                            ? 'text-emerald'
                            : 'text-silver'}"
                        onclick={toggleMenu}
                    >
                        {link.label}
                    </a>
                {/each}
            </nav>
        </div>
    {/if}
</header>
