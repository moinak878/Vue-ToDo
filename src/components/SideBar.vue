<template>
	<div>
		<h1>user Name</h1>
		<ol>
			<l1>To Do</l1>
			<l1>Completed</l1>
			<l1>Urgent</l1>
		</ol>
	</div>
</template>

<script>
export default {
	name: "SideBar",
};
</script>

<style scoped>
div {
	border: solid red 0.5em;
	padding: 10px;
	background: #dbdfe5;
	-webkit-flex: 1; /* Safari */
	-ms-flex: 1; /* IE 10 */
	flex: 1; /* Standard syntax */
	display: flex;
	flex-direction: column;
}
h1{
	flex: 1; /* Standard syntax */
}
ol{
	flex:1;
	display:flex;
	flex-direction: column;
	border: solid red 0.5rem;
}
</style>
