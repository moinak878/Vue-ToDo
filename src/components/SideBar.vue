<template>
	<div>
		<img class="user-image" v-bind:src="getImgUrl(username)" />
		<h2>@{{ username }}</h2>
		<ol>
			<l1><p>Profile</p></l1>
			<l1><p>ToDos</p></l1>
			<l1><p>Completed</p></l1>
			<l1><p>Urgent</p></l1>
			<l1><p>Groups</p></l1>
		</ol>
		<button class="addtask" @click="AddTask">Add Task</button>
	</div>
</template>

<script>
export default {
	name: "SideBar",
	data: function() {
		return {
			username: "moinak878",
		};
	},
	methods: {
		getImgUrl(pic) {
			return require("../assets/" + pic + ".jpg");
		},
	},
};
</script>

<style scoped>
div {
	overflow: hidden;
	z-index: 2;
	position: fixed;
	width: 20%;
	height: 100vh;
	padding: 0px;
	background: linear-gradient(to bottom, black, grey);
	-webkit-flex: 1; /* Safari */
	-ms-flex: 1; /* IE 10 */
	flex: 1; /* Standard syntax */
	display: flex;
	flex-direction: column;
	overflow: hidden;
}

.user-image {
	display: block;
	border-radius: 50%;
	padding: auto;
	margin: 10px auto auto auto;
	height: 150px;
	width: 150px;
}
h2 {
	flex: 1; /* Standard syntax */
	color: whitesmoke;
}
ol {
	flex: 1;
	display: flex;
	flex-direction: column;
	margin: auto 0 80% 0;
	padding: 10px 0px 0px 0px;
	justify-content: center;
	align-items: center;
}

ol l1 {
	/* padding: 10px auto 10px auto; */
	margin: 0 0 5px 0;
	flex: 1;
	width: 100%;
	display: flex;
	flex-direction: row;
	height: 70%;
	box-shadow: 1px 1px 1px 1px rgb(138, 135, 135);
}

ol l1:hover {
	background: linear-gradient(to right, #bdc3c7, #080808);
	box-shadow: 1px 1px 1px 1px rgb(219, 215, 215);
	scale: 1.12;
	cursor: pointer;
}

ol l1 p {
	flex: 1;
	margin: 5px 5px;
	width: 80%;
	color: white;
}

.addtask {
	position: relative;
	margin: auto 30px 50px 30px;
	height: 40px;
	border-radius: 0.5rem;
	border: solid white 1px;
	background: linear-gradient(to left, black, rgb(172, 169, 169));
	color: white;
	cursor: pointer;
}
</style>
