<template>
	<header>
		<div class="row align-items-center h-100">
			<div class="col-6 d-flex align-items-center">
				<img src="../assets/img/logo.png" alt="" />
			</div>
			<div class="col-6 d-flex align-items-center justify-content-end">
				<input class="align-self-end" type="select" />
			</div>
		</div>
	</header>
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
}
img {
	height: 50px;
}
</style>
