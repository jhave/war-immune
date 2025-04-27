<script>
	import ScrollStep from '$lib/components/ScrollStep.svelte';
</script>

<section class="h-[200vh] bg-black text-white">
	<h1 class="sticky top-10 text-4xl pl-8">Immune system · micro layer</h1>

	<ScrollStep index={0}>
		<p class="max-w-xl text-lg">
			Naïve T-cells patrol, sampling peptide fragments…
		</p>
	</ScrollStep>

	<ScrollStep index={1}>
		<p class="max-w-xl text-lg">
			Dysregulated tagging ⇒ cytokine storm.
		</p>
	</ScrollStep>
</section>