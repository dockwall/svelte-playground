<script lang="ts">
	const COLORS = ['red', 'green', 'blue', 'yellow'];
	let i = 0;
	$: color = COLORS[i];

	function changeColor(tick: number): void {
		setInterval(() => {
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
	}
</style>
