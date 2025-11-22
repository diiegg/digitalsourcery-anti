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
    class="fixed w-full top-0 z-50 bg-void/80 backdrop-blur-md border-b border-white/5"
>
    <div class="container mx-auto px-4">
        <div class="flex items-center justify-between h-20">
            <!-- Logo -->
            <a
                href="/"
                class="text-2xl font-display font-bold text-white tracking-widest hover:text-mana transition-colors"
            >
                DIGITAL<span class="text-mana">SORCERY</span>
            </a>

            <!-- Desktop Nav -->
            <nav class="hidden md:flex items-center space-x-8">
                {#each links as link}
                    <a
                        href={link.href}
                        class="text-sm font-mono uppercase tracking-wider hover:text-mana transition-colors {$page
                            .url.pathname === link.href
                            ? 'text-mana'
                            : 'text-gray-400'}"
                    >
                        {link.label}
                    </a>
                {/each}
                <Button
                    href="/contact"
                    variant="secondary"
                    class="ml-4 !py-2 !px-4 !text-xs"
                >
                    Summon Us
                </Button>
            </nav>

            <!-- Mobile Menu Button -->
            <button
                class="md:hidden text-white p-2"
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
        <div class="md:hidden bg-void border-b border-white/10">
            <nav class="flex flex-col p-4 space-y-4">
                {#each links as link}
                    <a
                        href={link.href}
                        class="text-sm font-mono uppercase tracking-wider hover:text-mana transition-colors {$page
                            .url.pathname === link.href
                            ? 'text-mana'
                            : 'text-gray-400'}"
                        onclick={toggleMenu}
                    >
                        {link.label}
                    </a>
                {/each}
            </nav>
        </div>
    {/if}
</header>
