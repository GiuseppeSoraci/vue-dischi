<template>
	<div id="app">
		<!-- Header -->
		<Header />

		<!-- Main -->
		<Main />
		<Disc />
	</div>
</template>

<script>
	import Header from "@/components/Header.vue";
	import Main from "@/components/Main.vue";
	import Disc from "@/components/Disc.vue";

	export default {
		name: "App",
		components: {
			Header,
			Main,
			Disc,
		},
	};
</script>

<style>
	/* Generals */
	* {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	/* Layout */
	body {
		font-family: Arial, Helvetica, sans-serif;
		font-weight: 400;
	}

	a {
		color: #f7fbfa;
		text-decoration: none;
	}

	/* Utilities */
	.container {
		max-width: 100%;
		margin: 0 auto;
	}

	.flex {
		display: flex;
	}
</style>
