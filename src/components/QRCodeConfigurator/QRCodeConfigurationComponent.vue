<template>
	<div class="align-center text-center align-middle QR__code_configuration__component">
		<div class="QR__code_configuration__component__content">
			<h1 class="mb-3">Created QR code</h1>
			<img src="https://picsum.photos/300/300" class="mb-3 ml-auto mr-auto" alt="generated_QR_Code" />
			<button class="bg-appMainColor text-white font-bold py-2 px-4 rounded inline-flex items-center">
				<svg class="fill-current w-4 h-4 mr-2" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
					<path d="M13 8V2H7v6H2l8 8 8-8h-5zM0 18h20v2H0v-2z" />
				</svg>
				<span>Download</span>
			</button>
		</div>
	</div>
</template>

<script lang="ts">
	import { Component, Prop, Vue } from "vue-property-decorator";

	@Component
	export default class QRCodeConfiguration extends Vue {
		@Prop() private msg!: string;
		firstName = "Brent";
		lastName = "Vanwildemeersch";
		get fullName() {
			return this.firstName + " " + this.lastName;
		}
	}
</script>

<style lang="scss" scoped>
	.QR__code_configuration__component {
		position: relative;
		.QR__code_configuration__component__content {
			position: relative;
			transform: translateY(-50%);
			top: 50%;
		}
	}
</style>