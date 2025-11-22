<script lang="ts">
    import TileBand from "./TileBand.svelte";
</script>

<section
    class="relative min-h-[80vh] flex flex-col justify-center overflow-hidden bg-andalus-night text-moonlight-ivory"
>
    <!-- Starfield Background -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
        <div
            class="absolute inset-0 bg-[radial-gradient(circle_at_center,_var(--color-tile-lapis)_0%,_transparent_50%)] opacity-20"
        ></div>
        <div
            class="stars absolute inset-0 animate-spin-slow opacity-60"
            style="background-image: radial-gradient(white 1px, transparent 1px); background-size: 50px 50px;"
        ></div>
    </div>

    <div
        class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24 grid grid-cols-1 lg:grid-cols-2 gap-12 items-center"
    >
        <div class="space-y-8">
            <div
                class="inline-flex items-center gap-2 px-3 py-1 rounded-full border border-caliphate-gold/30 bg-caliphate-gold/10 text-caliphate-gold text-sm font-medium"
            >
                <span
                    class="w-2 h-2 rounded-full bg-caliphate-gold animate-pulse"
                ></span>
                Platform Engineering & Automation
            </div>

            <h1
                class="font-display font-bold text-5xl lg:text-7xl leading-tight tracking-tight"
            >
                Digital <span
                    class="text-transparent bg-clip-text bg-gradient-to-r from-caliphate-gold to-citrus-ocher"
                    >Sorcery</span
                >
            </h1>

            <p class="text-lg text-stone-column max-w-xl leading-relaxed">
                Constructing the observatories of the digital age. We blend
                ancient wisdom with modern automation to build resilient,
                scalable platforms.
            </p>

            <div class="flex flex-wrap gap-4 pt-4">
                <a
                    href="/services"
                    class="bg-mezquita-red text-moonlight-ivory px-8 py-4 rounded-lg font-bold hover:bg-red-700 transition-all shadow-lg shadow-mezquita-red/20 hover:shadow-mezquita-red/40 hover:-translate-y-1"
                >
                    Explore Rituals
                </a>
                <a
                    href="/approach"
                    class="px-8 py-4 rounded-lg font-bold border border-stone-column/30 hover:border-caliphate-gold text-moonlight-ivory hover:text-caliphate-gold transition-all"
                >
                    Our Grimoire
                </a>
            </div>
        </div>

        <div class="relative hidden lg:block">
            <!-- Abstract Astrolabe / Observatory Illustration Placeholder -->
            <div
                class="aspect-square rounded-full border border-white/10 relative animate-spin-slower"
            >
                <div
                    class="absolute inset-4 rounded-full border border-white/5 border-dashed"
                ></div>
                <div
                    class="absolute inset-12 rounded-full border border-caliphate-gold/20"
                ></div>
                <div
                    class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-4 h-4 bg-caliphate-gold rounded-full shadow-[0_0_20px_rgba(215,164,74,0.5)]"
                ></div>

                <!-- Orbiting elements -->
                <div
                    class="absolute top-0 left-1/2 -translate-x-1/2 -translate-y-1/2 w-3 h-3 bg-tile-lapis rounded-full"
                ></div>
                <div
                    class="absolute bottom-12 right-12 w-2 h-2 bg-garden-emerald rounded-full"
                ></div>
            </div>
        </div>
    </div>

    <div class="absolute bottom-0 w-full">
        <TileBand />
    </div>
</section>

<style>
    .animate-spin-slow {
        animation: spin 120s linear infinite;
    }
    .animate-spin-slower {
        animation: spin 180s linear infinite reverse;
    }
    @keyframes spin {
        from {
            transform: rotate(0deg);
        }
        to {
            transform: rotate(360deg);
        }
    }
</style>
