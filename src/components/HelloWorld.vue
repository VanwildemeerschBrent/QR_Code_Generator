<template>
	<div class="hello bg-red-300">
		<h1>{{ msg }}</h1>
		<h4>{{fullName}}</h4>
	</div>
</template>

<script lang="ts">
	import { Component, Prop, Vue } from "vue-property-decorator";

	@Component
	export default class HelloWorld extends Vue {
		@Prop() private msg!: string;
		firstName = "Brent";
		lastName = "Vanwildemeersch";
		get fullName() {
			return this.firstName + " " + this.lastName;
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
	h3 {
		margin: 40px 0 0;
	}
	ul {
		list-style-type: none;
		padding: 0;
	}
	li {
		display: inline-block;
		margin: 0 10px;
	}
	a {
		color: #42b983;
	}
</style>
