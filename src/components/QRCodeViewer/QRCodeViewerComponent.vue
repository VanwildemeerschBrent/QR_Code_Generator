<template>
	<div class="p-4 rounded-md">
		<p>QR Code viewer component</p>
	</div>
</template>

<script lang="ts">
	import { Component, Prop, Vue } from "vue-property-decorator";

	@Component
	export default class QRCodeViewerComponent extends Vue {
		@Prop() private msg!: string;
		firstName = "Brent";
		lastName = "Vanwildemeersch";
		get fullName() {
			return this.firstName + " " + this.lastName;
		}
	}
</script>

<style scoped>
</style>