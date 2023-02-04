<script lang="ts">
	// Basic types
	const greeter: string = 'Hello Playground';
	const isPlayground: boolean = true;
	let ftNumber: number = 42;

	const numbersArr: number[] = [1, 2, 3, 4, 5];
	const genericAnyArr: Array<any> = [6, 9, 'this is string', true];

	function showMessage(message: string): string {
		return message;
	}

	// Tuple
	const nameIdArr: [string, number] = ['Earth', 3];

	const basicOutput: any = {
		title: 'This is basic types',
		greeter,
		isPlayground,
		ftNumber,
		numbersArr,
		genericAnyArr,
		showMessage,
		nameIdArr
	};

	// Custom types
	type Username = string;
	type ID = string | number;

	const defaultUsername: Username = 'anon';
	const stringID: ID = 'a12345';
	const numericID: ID = 12345;

	const customOutput: any = {
		title: 'This is custom types',
		defaultUsername,
		stringID,
		numericID
	};

	// Interfaces
	interface Cat {
		readonly id: number | string;
		color: string;
		name?: string;

		temperament: {
			aggressiveness: boolean;
			affectionateness: boolean;
		};
	}

	const myCat: Cat = {
		id: 1,
		color: 'silver',

		temperament: {
			aggressiveness: false,
			affectionateness: true
		}
	};

	const interfaceOutput: any = {
		title: 'This is interfaces',
		myCat
	};
</script>

<h1>This is TypeScript Playground section</h1>
<code class="output">
	{#each Object.entries(basicOutput) as stringArr, index}
		<span>{index + 1}| {stringArr[0]}: {typeof stringArr[1]} => {stringArr[1]}</span>
		<br />
	{/each}
	<hr />
	{#each Object.entries(customOutput) as stringArr, index}
		<span>{index + 1}| {stringArr[0]}: {typeof stringArr[1]} => {stringArr[1]}</span>
		<br />
	{/each}
	<hr />
	{#each Object.entries(interfaceOutput) as stringArr, index}
		<span>{index + 1}| {stringArr[0]}: {typeof stringArr[1]} => {stringArr[1]}</span>
		<br />
	{/each}
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
