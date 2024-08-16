<template>
	<div class="flex justify-center items-center h-screen flex-col">
		<div class="grid grid-cols-2 gap-2">
			<div
				class="w-[180px] h-[180px] bg-sky-500 flex items-center justify-center text-white"
				@mouseover="onLogEvent"
			>
				Mouse over event
			</div>
			<div
				@mouseleave="onLogEvent"
				class="w-[180px] h-[180px] bg-sky-500 flex items-center justify-center text-white"
			>
				Mouse leave
			</div>
			<div
				@dblclick="onLogEvent"
				class="w-[180px] h-[180px] bg-sky-500 flex items-center justify-center text-white"
			>
				Dobule click event
			</div>
			<div
				class="w-[180px] h-[180px] bg-sky-500 flex items-center justify-center text-white"
			>
				Mouse over event
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {};
	},
	methods: {
		onLogEvent(e) {
			console.log("run event::::::::::", e);
		},
	},
};
</script>
