<template>
	<div class="album-card p-3 text-center">
		<img :src="poster" :alt="title" class="img-fluid" />
		<h4>{{ title }}</h4>
		<h5>{{ author }}</h5>
		<div class="text-muted">{{ year }}</div>
	</div>
</template>

<script>
export default {
	name: "AlbumsCard",
	props: ["poster", "title", "author", "year", "genre"],
};
</script>

<style scoped>
.album-card {
	background-color: rgb(46, 58, 70);
	height: 350px;
	max-width: 200px;
	margin: 20px 0;
}
h4 {
	text-transform: uppercase;
	color: white;
}
</style>
