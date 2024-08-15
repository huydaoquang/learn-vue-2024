<template>
	<div class="flex justify-center items-center flex-col h-screen">
		<p>{{ hello("huydaoquang") }}</p>
		<p>{{ xinChao("huy") }}</p>

		<button
			@click="tangSo"
			type="button"
			class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800"
		>
			tang
		</button>
		<button
			@click="giamSo"
			type="button"
			:disabled="isDisabled"
			class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800"
		>
			giam
		</button>

		<span>{{ count }}</span>
	</div>
</template>

<script>
export default {
	data() {
		return {
			full_name: "daoquanghuy",
			count: 0,
			isDisabled: false,
		};
	},
	methods: {
		hello(fullName) {
			return "xin chao " + fullName;
		},
		xinChao: (name) => {
			return "xin chao " + name;
		},
		tangSo() {
			this.count++;
			this.isDisabled = this.count <= 0 ? true : false;
		},
		giamSo() {
			if (this.count > 0) {
				this.isDisabled = this.count <= 0 ? true : false;
				this.count--;
			}
		},
	},
};
</script>
