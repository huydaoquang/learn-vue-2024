<template>
	<div class="flex justify-center items-center h-screen">
		<form action="" @submit.prevent="formSubmit" class="flex flex-col">
			name: <input type="text" v-model="formData.name" /> email:
			<input type="text" v-model="formData.email" />
			<button>submit</button>
		</form>
	</div>
</template>

<script>
export default {
	data() {
		return {
			formData: {
				name: "",
				email: "",
			},
		};
	},
	methods: {
		formSubmit() {
			console.log(this.formData);
		},
	},
};
</script>
