<template>
	<div class="card flex">
		<div class="flex">
			<img :src="info.poster" :alt="info.title" />
		</div>
		<div class="details">
			<h3>
				<a href="#">{{ info.title }}</a>
			</h3>
			<div>{{ info.author }}</div>
			<div>{{ info.year }}</div>
			<a href="#">{{ info.genre }}</a>
		</div>
	</div>
</template>

<script>
	export default {
		name: "Disc",
		props: ["info"],
	};
</script>

<style scoped lang="scss">
	.card {
		width: 170px;
		height: 340px;
		padding-top: 10px;
		background: #2e3a46;
		margin: 15px;
		align-items: center;
	}
	img {
		width: 130px;
	}
	.details {
		text-align: center;
		padding: 10px 10px;
		div {
			padding: 5px 0;
			color: white;
			font-size: 14px;
		}
	}
	h3 {
		font-weight: 400;
		font-size: 20px;
		text-transform: uppercase;
		margin: 10px 0;
	}
</style>
