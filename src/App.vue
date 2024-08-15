<template>
	<div class="flex justify-center items-center flex-col h-screen">
		<div class="w-[500px]">
			<h1>{{ title }}</h1>
			<input
				v-model="title"
				type="email"
				id="email"
				class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
			/>
			<div class="flex gap-5">
				<button :disabled="isDisabled" class="bg-red-500">
					button disable
				</button>
				<button :disabled="isNotDisabled" class="bg-red-500">button</button>
			</div>
			<a :href="link" class="underline text-sky-300">click to google.com</a>
			<img :src="imgLink" alt="" />
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			imgLink:
				"https://res.klook.com/image/upload/c_fill,w_1265,h_712/q_80/w_80,x_15,y_15,g_south_west,l_Klook_water_br_trans_yhcmh3/activities/tsah7c9evnal289z5fig.webp",
			link: "https://google.com",
			isDisabled: true,
			isNotDisabled: false,
		};
	},
};
</script>
