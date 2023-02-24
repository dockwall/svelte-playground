<script lang="ts">
	const COLORS = ['red', 'green', 'blue', 'yellow'];
	let i = 0;
	$: color = COLORS[i];

	let timerID: ReturnType<typeof setTimeout>;

	function changeColor(tick: number): void {
		timerID = setInterval(() => {
			if (i >= COLORS.length - 1) {
				i = 0;
			} else {
				i++;
			}
		}, tick);
	}

	changeColor(1000);
</script>

<div class="colorful-pixel colorful-pixel--{color}" />
<button class="colorful-pixel__button" on:click={() => clearInterval(timerID)}>Stop Pixel</button>

<style lang="scss">
	.colorful-pixel {
		height: 50px;
		width: 50px;
		border: 3px dashed black;

		&--red {
			background-color: red;
		}

		&--green {
			background-color: green;
		}

		&--blue {
			background-color: blue;
		}

		&--yellow {
			background-color: yellow;
		}

		&__button {
			margin-top: 10px;
			background-color: white;
			border: 1px solid gray;
		}
	}
</style>
