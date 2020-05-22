<template>
	<div class>
		<p>QR Code configurator</p>
	</div>
</template>

<script lang="ts">
	import { Component, Prop, Vue } from "vue-property-decorator";

	@Component
	export default class QRCodeConfiguration extends Vue {
		@Prop() private msg!: string;
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