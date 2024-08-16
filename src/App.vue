<template>
	<div class="flex justify-center items-center h-screen flex-col">
		<p>methods: {{ fullName() }}</p>
		<p>computed: {{ fullNameComputed }}</p>
		<button @click="changeFullName">Click</button>

		<p>{{ count }}</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			count: 0,
			firstName: "",
			lastName: "",
		};
	},
	methods: {
		tangSo() {
			this.count++;
		},
		fullName() {
			console.log("fullName Method");
			return this.firstName + " " + this.lastName;
		},
		changeFullName() {
			this.fullNameComputed = "huy.daoquang";
		},
	},
	computed: {
		fullNameComputed: {
			get() {
				return this.firstName + " " + this.lastName;
			},
			set(value) {
				console.log("fullName computed");
				this.firstName = value;
			},
		},
	},
};
</script>
