<template>
	<StackLayout class="fab-button" :backgroundColor="color">
		<GridLayout rows="2, auto" horizontalAlignment="center" class="fab-icon iconIdle">
			<Image v-if="loaded" class="fab-dash" stretch="none" row="1" :src="image" />
		</GridLayout>
	</StackLayout>
</template>


<script>
	export default {
		props: {
			icon: {
				type: String,
				required: true
			},
			color: {
				type: String,
				required: true,
				default: "orangered"
			}
		},
		data: () => ({
			image: '',
			loaded: false
		}),
		mounted () {
			this.image = this.icon
			this.loaded = true
		}
	};
</script>

<style scoped>
	.fab-button {
		width: 56;
		height: 56;
		background-color: orangered;
		border-radius: 28;
		vertical-align: center;
		box-shadow: 10px 10px 5px grey;
	}

	.fab-icon {
		height: 16;
		width: 16;
	}

	.fab-dash {
		background-color: #fff;
		height: 16;
		width: 3;
	}
.iconActive {
		animation-name: iconActive;
		animation-duration: .25;
		animation-timing-function: cubic-bezier(0.165, 0.840, 0.440, 1.000);
		animation-fill-mode: forwards;
	}

	.iconIdle {
		animation-name: iconActive;
		animation-duration: .25;
		animation-timing-function: ease-out;
		animation-fill-mode: forwards;
		animation-direction: reverse;
	}

	@keyframes iconActive {
		from {
			transform: rotate(0deg);
		}
		to {
			transform: rotate(225deg);
		}
	}
</style>