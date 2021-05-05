<template>
	<ul>
		<li><a href="#">Todos</a></li>
		<li><a href="#">About Us</a></li>
		<li><a href="#">Settings</a></li>
		<li><a href="#">Logout</a></li>
	</ul>
</template>

<script>
export default {
	name: "Header",
};
</script>

<style scoped>
ul {
	/* border: solid green 0.5rem; */
	background: linear-gradient(to right, black, rgb(42, 41, 41));
	padding: 10px;
	flex: 1;
	margin: 0 20%;
	width: 80%;
	max-height: 5%;
	display: flex;
	flex-direction: row;
	align-items: flex-end;
	overflow: hidden;
	position: fixed;
	z-index: 2;
}
.light {
	background: linear-gradient(to bottom, blue, grey);
}
ul li {
	flex: 1;
	list-style-type: none;
	padding: 5px;
	margin: auto 5rem;
}
ul li a {
	width: 100%;
	padding: 5px;
	text-decoration: none;
	display: block;
	color: white;
}
</style>
