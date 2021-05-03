<template>
	<div class="main-container">
		<SideBar />
		<div class="view">
			<Header />
			<TaskDisplay />
		</div>
	</div>
	<!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
	<!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import SideBar from "./components/SideBar.vue";
import Header from "./components/Header.vue";
import TaskDisplay from "./components/TaskDisplay.vue";

export default {
	name: "App",
	components: {
		HelloWorld,
		SideBar,
		Header,
		TaskDisplay,
	},
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
}
.main-container {
	position: absolute;
	width: 100%;
	min-height: 100vh;
	overflow: visible;
	display: -webkit-flex; /* Safari */
	display: flex; /* Standard syntax */
}
.view {
	width: 80%;
	display: flex;
	flex-direction: column;
	border: solid orange 0.5rem;
}
</style>
