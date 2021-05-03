<template>
	<!-- display all tasks here  -->
	<div class="tasks">
		<h1>tasks</h1>
		<button @click="AddTask">Add Task</button>
	</div>
</template>

<script>
export default {
	name: "TaskDisplay",
	methods: {
		AddTask: function() {
			console.log("click me!");
		},
	},
};
</script>

<style scoped>
.tasks {
	border: solid blue 0.5rem;
	padding: 10px;
	background: #dbdfe5;
	-webkit-flex: 1; /* Safari */
	-ms-flex: 1; /* IE 10 */
	flex: 1; /* Standard syntax */
	margin: 0 0;
    
}
.tasks h1{
    margin: auto auto;
    padding : 10px;
}
.tasks button{
    position: absolute;
    margin :35% -5%;
    background: green;
    height: 50px;
    width:100px;
    border-radius: 0.5rem;
    padding : 0 ;
}
</style>
