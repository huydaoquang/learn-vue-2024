<template>
	<div id="app" class="flex justify-center items-center h-screen">
		<button
			@click="showModal = true"
			class="bg-green-500 text-white px-2 py-1 rounded-md"
		>
			Open Modal
		</button>
		<Modal :isVisible="showModal" @close="showModal = false">
			<div class="flex flex-col">
				<h2 class="font-bold">ダウンロード情報</h2>
				<div class="border-2 border-black border-opacity-60 p-5 pb-12">
					<div class="grid grid-cols-1 md:grid-cols-2 gap-5">
						<p>
							<span class="font-bold">ダウンロード日時</span> &nbsp;
							2024/01/0112:00:00
						</p>
						<p>
							<span class="font-bold">ダウンロード日時</span> &nbsp;
							XXXXXXXXXXXXX
						</p>
						<p>
							<span class="font-bold">ダウンロード日時</span> &nbsp; 店舗・DPT
						</p>
					</div>

					<div class="md:p-8 grid grid-cols-1 md:grid-cols-2 gap-10">
						<div>
							<span class="font-bold">店舗</span>
							<div
								class="border border-black border-opacity-50 grid grid-cols-1 md:grid-cols-2 pl-5 p-2 pb-9 gap-2"
							>
								<span>0003-XXXXXXXX</span>
								<span>0003-XXXXXXXX</span>
								<span>0003-XXXXXXXX</span>
								<span>0003-XXXXXXXX</span>
							</div>
						</div>
						<div>
							<span class="font-bold">DPT</span>
							<div
								class="border border-black border-opacity-50 grid grid-cols-1 md:grid-cols-2 pl-5 p-2 pb-9 gap-2"
							>
								<span>0003-XXXXXXXX</span>
								<span>0003-XXXXXXXX</span>
								<span>0003-XXXXXXXX</span>
								<span>0003-XXXXXXXX</span>
							</div>
						</div>
					</div>
					<p>
						<span class="font-bold">ダウンロードファイル</span> &nbsp;
						XXXXXXXXXXXXXXX.xlsx
					</p>
				</div>
				<h2 class="mt-5 font-bold">登録情報</h2>
				<div class="border-2 border-black border-opacity-60 p-8">
					<div class="grid grid-cols-1 md:grid-cols-2 gap-5">
						<p>
							<span class="font-bold">登録日時</span> &nbsp; 2024/01/0112:00:00
						</p>
						<p><span class="font-bold">登録者 </span> &nbsp; XXXXXXXXXXXXX</p>
						<p>
							<span class="font-bold">登録ファイル</span> &nbsp;
							XXXXXXXXXXXXXXX.xlsx
						</p>
					</div>
				</div>
			</div>
		</Modal>
	</div>
</template>

<script>
import Modal from "./components/modals/ModalDetail.vue";

export default {
	components: {
		Modal,
	},
	data() {
		return {
			showModal: false,
		};
	},
};
</script>
