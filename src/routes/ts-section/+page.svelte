<script lang="ts">
	import { each } from 'svelte/internal';

	const greeter: string = 'Hello Playground';
	const isPlayground: boolean = true;
	let ftNumber: number = 42;

	const output: any = {
		greeter,
		isPlayground,
		ftNumber
	};
</script>

<h1>This is TypeScript Playground section</h1>
<code class="output">
	{#each Object.entries(output) as stringArr, index}
		<span>{index + 1}| {stringArr[0]}: {typeof stringArr[1]} => {stringArr[1]}</span>
		<br />
	{/each}
</code>
<hr />

<p>Back to <a href="/">Root Page</a></p>

<style lang="scss">
	.output {
		display: block;
		padding: 10px;
		width: 75%;
		border: solid 2px black;
		border-radius: 5px;
		background-color: #2f677a;
		color: lightcyan;
		font-size: 18px;
	}
</style>
