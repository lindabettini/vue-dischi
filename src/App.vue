<template>
	<div>
		<Header :albums="albums" @updateValue="updateValue" />
		<Main :albums="albums" :selectedValueChoose="selectedValueChoose" />
	</div>
</template>

<script>
import axios from "axios";

import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
export default {
	name: "App",
	components: {
		Header,
		Main,
	},
	data() {
		return {
			selectedValueChoose: "",
			albums: [],
		};
	},
	methods: {
		updateValue(value) {
			this.selectedValueChoose = value;
		},
	},
	created() {
		axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((res) => {
			this.albums = res.data.response;
		});
	},
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
