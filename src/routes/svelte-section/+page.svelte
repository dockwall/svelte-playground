<script lang="ts">
	import ColorfulPixel from '$lib/components/ColorfulPixel.svelte';

	const name: string = 'xD';
</script>

<div class="svelte-playground">
	<h1>This is Svelte Playground Section</h1>

	<p>Name value => {name}</p>

	<img src="/joker.jpg" alt="{name} jokir" class="svelte-playground__img" />

	<ColorfulPixel />

	<hr />

	<p>Back to <a href="/">Root Page</a></p>
</div>

<style lang="scss">
	.svelte-playground {
		&__img {
			height: 200px;
		}
	}
</style>
