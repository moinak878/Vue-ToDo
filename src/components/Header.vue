<template>
	<ul>
		<li> <a href="#">Todos</a></li>
		<li> <a href="#">About Us</a></li>
		<li> <a href="#">Settings</a></li>
		<li> <a href="#">Logout</a></li>
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
	background-image: linear-gradient(to right , rgb(64, 97, 187) ,rgb(194, 212, 236));
	padding: 10px;
	-webkit-flex: 1; /* Safari */
	-ms-flex: 1; /* IE 10 */
	flex: 1; /* Standard syntax */
	margin: 0;
	max-height: 5%;
	display: flex;
	flex-direction: row;
	align-items: flex-end;
}
ul li{
	flex : 1;
	list-style-type: none;
	padding : 5px;
	margin : auto 5rem;
}
ul li a{
	width : 100%;
	padding : 5px;
	text-decoration: none;
	display: block;
	color: black;

}
</style>
