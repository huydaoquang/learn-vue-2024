v-for :key :src

<template>
	<div class="flex justify-center items-center h-screen flex-col">
		<div class="grid grid-cols-2 gap-2">
			<div
				class="w-[180px] h-[180px] flex items-center justify-center text-white flex-col"
				v-for="product in productsFilter"
				:class="product.isCart ? 'bg-red-400' : 'bg-sky-500'"
				:key="product.id"
				@dblclick="onToggleCart($event, product)"
			>
				<img :src="product.thumbnail" alt="" />
				<h3>name: {{ product.name }}</h3>
				<p>price:{{ product.price }}</p>
			</div>
		</div>
	</div>
</template>

<style scoped>
.cart {
	background-color: chartreuse;
}
</style>

<script>
export default {
	data() {
		return {
			img: "gg.com",
			products: [
				{
					id: 1,
					isCart: false,
					name: "Product A",
					price: 1030,
					thumbnail:
						"https://images.unsplash.com/photo-1723466394553-f52d59876483?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8",
				},
				{
					id: 2,
					isCart: true,
					name: "Product B",
					price: 1570,
					thumbnail:
						"https://images.unsplash.com/photo-1723466394553-f52d59876483?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8",
				},
				{
					id: 3,
					isCart: true,
					name: "Product C",
					price: 2000,
					thumbnail:
						"https://images.unsplash.com/photo-1723466394553-f52d59876483?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8",
				},
				{
					id: 4,
					isCart: true,
					name: "Product D",
					price: 2850,
					thumbnail:
						"https://images.unsplash.com/photo-1723466394553-f52d59876483?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8",
				},
				{
					id: 5,
					isCart: false,
					name: "Product E",
					price: 300,
					thumbnail:
						"https://images.unsplash.com/photo-1723466394553-f52d59876483?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8",
				},
			],
		};
	},
	methods: {
		onToggleCart(e, product) {
			product.isCart = !product.isCart;
			console.log("product.isCart", product.isCart);
		},
	},
	computed: {
		productsFilter() {
			return this.products.filter((product) => product.price > 300);
		},
	},
};
</script>
