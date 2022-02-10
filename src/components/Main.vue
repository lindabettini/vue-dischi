<template>
	<main>
		<div class="container">
			<section id="albums"></section>
		</div>
	</main>
</template>

<script>
import axios from "axios";
export default {
	name: "Main",
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
