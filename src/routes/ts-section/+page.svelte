<script lang="ts">
	const greeter: string = 'Hello Playground';
	const isPlayground: boolean = true;
	let ftNumber: number = 42;

	const numbersArr: number[] = [1, 2, 3, 4, 5];
	const genericAnyArr: Array<any> = [6, 9, 'this is string', true];

	function showMessage(message: string): string {
		return message;
	}

	const output: any = {
		greeter,
		isPlayground,
		ftNumber,
		numbersArr,
		genericAnyArr,
		showMessage
	};
</script>

<h1>This is TypeScript Playground section</h1>
<code class="output">
	{#each Object.entries(output) as stringArr, index}
		<span>{index + 1}| {stringArr[0]}: {typeof stringArr[1]} => {stringArr[1]}</span>
		<br />
	{/each}
	<br />
</code>
<br />
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
