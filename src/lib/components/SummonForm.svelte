<script lang="ts">
    import WorkshopSection from "./WorkshopSection.svelte";
</script>

<WorkshopSection variant="dark" id="contact">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
        <div>
            <h2
                class="font-display font-bold text-3xl md:text-4xl mb-6 text-moonlight-ivory"
            >
                Summon the Circle
            </h2>
            <p class="text-stone-column text-lg mb-8 leading-relaxed">
                Ready to transform your infrastructure? Send a missive to our
                order. We typically respond within one solar rotation.
            </p>

            <div class="space-y-4 text-stone-column">
                <div class="flex items-center gap-3">
                    <span class="text-caliphate-gold">Email:</span>
                    <a
                        href="mailto:circle@digitalsorcery.io"
                        class="hover:text-moonlight-ivory transition-colors"
                        >circle@digitalsorcery.io</a
                    >
                </div>
                <div class="flex items-center gap-3">
                    <span class="text-caliphate-gold">Location:</span>
                    <span>Córdoba, Spain (Remote Worldwide)</span>
                </div>
            </div>
        </div>

        <form
            name="contact"
            method="POST"
            data-netlify="true"
            action="/success"
            class="space-y-6 bg-white/5 p-8 rounded-2xl border border-white/10 backdrop-blur-sm"
        >
            <input type="hidden" name="form-name" value="contact" />

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="space-y-2">
                    <label
                        for="name"
                        class="text-sm font-medium text-stone-column"
                        >Name</label
                    >
                    <input
                        type="text"
                        id="name"
                        name="name"
                        required
                        class="w-full bg-andalus-night/50 border border-white/10 rounded-lg px-4 py-3 text-moonlight-ivory focus:outline-none focus:border-caliphate-gold focus:ring-1 focus:ring-caliphate-gold transition-colors"
                    />
                </div>
                <div class="space-y-2">
                    <label
                        for="email"
                        class="text-sm font-medium text-stone-column"
                        >Email</label
                    >
                    <input
                        type="email"
                        id="email"
                        name="email"
                        required
                        class="w-full bg-andalus-night/50 border border-white/10 rounded-lg px-4 py-3 text-moonlight-ivory focus:outline-none focus:border-caliphate-gold focus:ring-1 focus:ring-caliphate-gold transition-colors"
                    />
                </div>
            </div>

            <div class="space-y-2">
                <label
                    for="company"
                    class="text-sm font-medium text-stone-column"
                    >Company / Guild</label
                >
                <input
                    type="text"
                    id="company"
                    name="company"
                    class="w-full bg-andalus-night/50 border border-white/10 rounded-lg px-4 py-3 text-moonlight-ivory focus:outline-none focus:border-caliphate-gold focus:ring-1 focus:ring-caliphate-gold transition-colors"
                />
            </div>

            <div class="space-y-2">
                <label
                    for="message"
                    class="text-sm font-medium text-stone-column">Message</label
                >
                <textarea
                    id="message"
                    name="message"
                    rows="4"
                    required
                    class="w-full bg-andalus-night/50 border border-white/10 rounded-lg px-4 py-3 text-moonlight-ivory focus:outline-none focus:border-caliphate-gold focus:ring-1 focus:ring-caliphate-gold transition-colors"
                ></textarea>
            </div>

            <button
                type="submit"
                class="w-full bg-mezquita-red text-moonlight-ivory font-bold py-4 rounded-lg hover:bg-red-700 transition-colors shadow-lg shadow-mezquita-red/20"
            >
                Send Missive
            </button>
        </form>
    </div>
</WorkshopSection>
