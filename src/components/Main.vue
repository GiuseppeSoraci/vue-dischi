<template>
	<main class="flex">
		<div class="container flex">
			<Disc v-for="(item, index) in discs.response" :key="index" :info="item" />
		</div>
	</main>
</template>

<script>
	import axios from "axios";
	import Disc from "@/components/Disc.vue";

	export default {
		name: "Main",
		components: {
			Disc,
		},
		data() {
			return {
				apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
				discs: [],
				loading: true,
			};
		},
		created() {
			this.getDiscs();
		},
		methods: {
			getDiscs() {
				axios
					.get(this.apiURL)
					.then((res) => {
						console.log(res.data);
						this.discs = res.data;
					})
					.catch((error) => {
						console.log(error);
					});
			},
		},
	};
</script>

<style scoped>
	main {
		background: #1d2d3c;
	}
	.container {
		padding-top: 100px;
	}

	.flex {
		justify-content: center;
		flex-wrap: wrap;
	}
</style>
