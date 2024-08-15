<!-- src/components/Modal.vue -->
<template>
	<transition name="fade">
		<div v-if="isVisible" class="modal-overlay" @click="handleOverlayClick">
			<div class="modal w-[900px]" @click.stop>
				<div class="flex items-start justify-between mt-[-10px]">
					<h1 class="text-2xl font-bold">自動発注停止ダウンロード・登録詳細</h1>
					<button @click="closeModal" class="text-orange-400 underline">
						閉じる
					</button>
				</div>
				<div class="modal-content">
					<slot></slot>
				</div>
			</div>
		</div>
	</transition>
</template>

<script>
export default {
	props: {
		isVisible: {
			type: Boolean,
			required: true,
		},
	},
	methods: {
		closeModal() {
			this.$emit("close");
		},
		handleOverlayClick() {
			this.closeModal();
		},
	},
};
</script>

<style scoped>
.modal-overlay {
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	background: rgba(0, 0, 0, 0.5);
	display: flex;
	justify-content: center;
	align-items: center;
}

.modal {
	background: white;
	padding: 20px 30px 50px;
	border-radius: 8px;
	max-width: 90%;
	position: relative;
}

.close-button {
	background: none;
	border: none;
	font-size: 24px;
	cursor: pointer;
	position: absolute;
	top: 10px;
	right: 10px;
}

.modal-content {
	margin-top: 20px;
}

/* Simple Fade Transition */
.fade-enter-active,
.fade-leave-active {
	transition: opacity 0.3s ease;
}

.fade-enter, .fade-leave-to /* .fade-leave-active trong phiên bản cũ */ {
	opacity: 0;
}
</style>
