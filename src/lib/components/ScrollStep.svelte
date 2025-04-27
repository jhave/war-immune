<script>
	import { onMount } from 'svelte';
	import { createEventDispatcher } from 'svelte';

	export let index = 0;
	const dispatch = createEventDispatcher();
	let el;

	onMount(() => {
		const io = new IntersectionObserver(
			([entry]) => entry.isIntersecting && dispatch('enter', { index }),
			{ threshold: 0.6 }
		);
		io.observe(el);
		return () => io.disconnect();
	});
</script>

<div bind:this={el} class="step h-screen flex items-center px-8">
	<slot />
</div>