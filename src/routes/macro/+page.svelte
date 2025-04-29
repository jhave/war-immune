<script>
	import ScrollStep from '$lib/components/ScrollStep.svelte';
	import InkPlayer   from '$lib/components/InkPlayer.svelte';

	let player;                // reference to InkPlayer instance

	function onStep() {
		player.advance();      // choose first available choice on each step
	}
</script>

<section class="h-[200vh] bg-white text-gray-900 px-8">
	<h1 class="sticky top-10 text-4xl">Nation-state · macro layer</h1>

	<!-- shared Ink narrative -->
	<InkPlayer bind:this={player} src="/autoimmune.json" class="mt-6 prose"/>

	<!-- scroll-triggered captions -->
	<ScrollStep index={0} on:enter={onStep}>
		<p class="max-w-xl text-lg">
			Border forces classify ingress as friend or enemy…
		</p>
	</ScrollStep>

	<ScrollStep index={1} on:enter={onStep}>
		<p class="max-w-xl text-lg">
			Mass mobilisation mirrors IL-6 surge.
		</p>
	</ScrollStep>
</section>