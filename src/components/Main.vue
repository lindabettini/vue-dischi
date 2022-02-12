<template>
	<main>
		<section id="albums" class="container">
			<div class="albums-list row">
				<div v-for="album in filteredAlbums" :key="album.title" class="col-3">
					<AlbumsCard :album="album" />
				</div>
			</div>
		</section>
	</main>
</template>

<script>
import AlbumsCard from "./AlbumsCard.vue";
export default {
	name: "Main",
	components: { AlbumsCard },
	props: ["albums", "selectedValueChoose"],
	computed: {
		filteredAlbums() {
			const selectedGenre = this.selectedValueChoose;
			return this.albums.filter((album) => {
				if (album.genre == selectedGenre || selectedGenre == "Tutti" || selectedGenre == "") {
					return true;
				}
			});
		},
	},
};
</script>

<style scoped lang="scss">
.albums-list {
	padding: 30px 100px;
}
</style>
