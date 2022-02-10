<template>
	<main>
		<section id="albums" class="container">
			<div class="albums-list row">
				<div v-for="album in albums" :key="album.title" class="col-5 col-md-3 col-lg-2">
					<AlbumsCard :poster="album.poster" :title="album.title" :author="album.author" :year="album.year" />
				</div>
			</div>
		</section>
	</main>
</template>

<script>
import axios from "axios";

import AlbumsCard from "./AlbumsCard.vue";
export default {
	name: "Main",
	components: { AlbumsCard },
	data() {
		return {
			albums: [],
		};
	},
	created() {
		axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((res) => {
			this.albums = res.data.response;
		});
	},
};
</script>

<style scoped lang="scss"></style>
