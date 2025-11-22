<script lang="ts">
	let { children } = $props();
</script>

<div class="min-h-screen bg-andalus-night text-moonlight-ivory flex flex-col font-body selection:bg-caliphate-gold selection:text-andalus-night">
	<header class="border-b border-white/10 bg-andalus-night/90 backdrop-blur sticky top-0 z-50">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
			<a href="/" class="font-display font-bold text-xl tracking-tight text-moonlight-ivory hover:text-caliphate-gold transition-colors">
				Digital Sorcery
			</a>
			<nav class="hidden md:flex gap-8 text-sm font-medium text-stone-column">
				<a href="/" class="hover:text-caliphate-gold transition-colors">Home</a>
				<a href="/services" class="hover:text-caliphate-gold transition-colors">Rituals</a>
				<a href="/approach" class="hover:text-caliphate-gold transition-colors">Grimoire</a>
				<a href="/case-studies" class="hover:text-caliphate-gold transition-colors">Spellbook</a>
				<a href="/insights" class="hover:text-caliphate-gold transition-colors">Scriptorium</a>
				<a href="/about" class="hover:text-caliphate-gold transition-colors">Circle</a>
			</nav>
			<a href="/contact" class="bg-mezquita-red text-moonlight-ivory px-4 py-2 rounded-md text-sm font-semibold hover:bg-red-700 transition-colors shadow-lg shadow-mezquita-red/20">
				Summon
			</a>
		</div>
	</header>

	<main class="flex-grow">
		{@render children()}
	</main>

	<footer class="bg-andalus-night border-t border-white/10 py-12 mt-auto">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-4 gap-8">
			<div class="col-span-1 md:col-span-2">
				<h3 class="font-display font-bold text-lg text-moonlight-ivory mb-4">Digital Sorcery</h3>
				<p class="text-stone-column text-sm max-w-xs leading-relaxed">
					Platform engineering and automation consulting services inspired by the wisdom of al-Andalus.
				</p>
			</div>
			<div>
				<h4 class="font-bold text-moonlight-ivory mb-4 text-sm uppercase tracking-wider">Navigation</h4>
				<ul class="space-y-2 text-sm text-stone-column">
					<li><a href="/services" class="hover:text-caliphate-gold transition-colors">Services</a></li>
					<li><a href="/approach" class="hover:text-caliphate-gold transition-colors">Approach</a></li>
					<li><a href="/case-studies" class="hover:text-caliphate-gold transition-colors">Case Studies</a></li>
				</ul>
			</div>
			<div>
				<h4 class="font-bold text-moonlight-ivory mb-4 text-sm uppercase tracking-wider">Connect</h4>
				<ul class="space-y-2 text-sm text-stone-column">
					<li><a href="/contact" class="hover:text-caliphate-gold transition-colors">Contact</a></li>
					<li><a href="https://github.com" class="hover:text-caliphate-gold transition-colors">GitHub</a></li>
					<li><a href="https://linkedin.com" class="hover:text-caliphate-gold transition-colors">LinkedIn</a></li>
				</ul>
			</div>
		</div>
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-12 pt-8 border-t border-white/5 text-center text-xs text-stone-column/60">
			© {new Date().getFullYear()} Digital Sorcery. All rights reserved.
		</div>
	</footer>
</div>
