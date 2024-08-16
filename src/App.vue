<template>
	<div class="flex justify-center items-center flex-col h-screen">
		<p>{{ name }} -- {{ age }}</p>

		<form action="" @submit.prevent="formSubmit">
			<button
				class="text-white bg-blue-700 hover:bg-blue-800 focus:outline-none focus:ring-4 focus:ring-blue-300 font-medium rounded-full text-sm px-5 py-2.5 text-center me-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
			>
				Submit
			</button>
			<input
				v-model="name"
				id="email"
				class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
				placeholder="name@flowbite.com"
				required
			/>
			<input
				v-model="age"
				id="email"
				class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
				placeholder="name@flowbite.com"
				required
			/>
		</form>
	</div>
</template>

<script>
export default {
	data() {
		return {
			name: "huy",
			age: 30,
		};
	},
	methods: {
		onChangeName(event) {
			// console.log("event: ", event);
			this.name = event.target.value;
		},
		formSubmit() {
			alert(this.name);
			alert(this.age);
		},
	},
};
</script>
