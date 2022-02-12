<template>
	<div class="album-card p-3 text-center">
		<img :src="album.poster" :alt="album.title" class="img-fluid" />
		<h4>{{ album.title }}</h4>
		<h5>{{ album.author }}</h5>
		<div class="text-muted">{{ album.year }}</div>
	</div>
</template>

<script>
export default {
	name: "AlbumsCard",
	props: ["album"],
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
