<template>
	<header>
		<div class="row align-items-center h-100">
			<div class="col-6 d-flex align-items-center">
				<img src="../assets/img/logo.png" alt="" />
			</div>
			<div class="col-6 d-flex align-items-center justify-content-end">
				<label for="genre">Choose a genre:</label>
				<select name="genre" id="select-genre" class="align-self-end">
					<option v-bind="genre[1]"></option>
				</select>
			</div>
		</div>
	</header>
</template>

<script>
import axios from "axios";

export default {
	name: "Header",
	data() {
		return {
			genre: [],
		};
	},
	created() {
		axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((res) => {
			this.genre = res.data.response.genre;
		});
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
