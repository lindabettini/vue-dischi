<template>
	<header><img src="../assets/img/logo.png" alt="" /></header>
</template>

<script>
export default {
	name: "Header",
};
</script>

<style scoped lang="scss">
header {
	height: 70px;
	background-color: rgb(46, 58, 70);
	padding: 0 40px;
	display: flex;
	align-items: center;
	img {
		height: 50px;
	}
}
</style>
