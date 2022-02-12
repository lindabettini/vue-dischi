<template>
	<header>
		<div class="row align-items-center h-100">
			<div class="col-6 d-flex align-items-center">
				<img src="../assets/img/logo.png" alt="" />
			</div>
			<div class="col-6 d-flex align-items-center justify-content-end">
				<label>Choose a genre:</label>
				<select id="select-genre" class="align-self-end">
					<option value="all">Tutti</option>
					<option v-for="(genre, index) in getUnicGenre()" :key="index" :value="genre">{{ genre }}</option>
				</select>
			</div>
		</div>
	</header>
</template>

<script>
export default {
	name: "Header",
	props: ["albums"],
	data() {
		return {};
	},
	methods: {
		getUnicGenre() {
			const genres = [];
			this.albums.forEach((album) => {
				if (!genres.includes(album.genre)) {
					genres.push(album.genre);
				}
			});
			return genres;
		},
	},
};
</script>

<style scoped lang="scss">
header {
	height: 70px;
	background-color: rgb(46, 58, 70);
	padding: 0 40px;
}
img {
	height: 50px;
}
</style>
