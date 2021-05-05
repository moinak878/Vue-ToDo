<template>
	<!-- display all tasks here  -->
	<div class="container">
		<div class="main-area">
			<transition-group name="list-complete" >
				<div class="task-card" v-for="task in tasks" v-bind:key="task.id">
					<span class="close" @click="deleteTask(key)">&times;</span>

					<img src="../assets/logo.png" />

					<p>{{ task.msg }}</p>
				</div>
			</transition-group>
		</div>
	</div>
</template>

<script>
export default {
	name: "TaskDisplay",
	data() {
		return {
			tasks: [
				{
					id: 1,
					msg: "This is sample task 1 that i have to complete by 1/1/2021",
				},
				{
					id: 2,
					msg: "This is sample task 1 that i have to complete by 2/1/2021",
				},
				{
					id: 3,
					msg: "This is sample task 1 that i have to complete by 3/1/2021",
				},
				{
					id: 4,
					msg: "This is sample task 1 that i have to complete by 4/1/2021",
				},
				{
					id: 5,
					msg: "This is sample task 1 that i have to complete by 5/1/2021",
				},
				{
					id: 6,
					msg: "This is sample task 1 that i have to complete by 6/1/2021",
				},
				{
					id: 7,
					msg: "This is sample task 1 that i have to complete by 7/1/2021",
				},
				{
					id: 8,
					msg: "This is sample task 1 that i have to complete by 8/1/2021",
				},
			],
		};
	},
	methods: {
		AddTask: function() {
			console.log("click me!");
		},
		deleteTask(key) {
			this.tasks.splice(key, 1);
		},
	},
};
</script>

<style scoped>
.container {
	width: 100%;
	margin: 1% auto 2% auto;
	overflow: auto;
	background: #dbdfe5;
	translate: 25% 5%;
	align-items: center;
	justify-content: center;
	height: 100%;
	background: linear-gradient(to right, #bdc3c7, #121518);
}
.main-area {
	display: flexbox;
	align-content: center;
	align-items: center;
	padding: 10px 10px;
	background: #dbdfe5;
	flex: 1;
	display: flex;
	justify-content: center;
	align-items: center;
	overflow-y: auto;
	flex-wrap: wrap;
	flex-grow: 1;
	background: linear-gradient(to right, #bdc3c7, #121518);
}
.task-card {
	min-width: 300px;
	max-width: 300px;
	position: relative;
	margin: 20px 15px;
	padding: 10px;
	background: linear-gradient(to bottom, gray, rgba(24, 24, 24, 0.383));
	border-radius: 1.125rem;
	flex: 1;
	display: flexbox;
	align-items: center;
	box-shadow: 2px 5px 5px 2px rgba(3, 2, 2, 0.5);
	cursor: pointer;
}
.task-card:hover {
	background: linear-gradient(to top, black, rgb(172, 169, 169));
	transform: scale(1.01);
	border: solid white 1px;
	box-shadow: 2px 5px 5px 2px rgba(23, 23, 24, 0.5);
	z-index: 5;
}
.task-card img {
	height: 30px;
	width: 30px;
	flex: 1;
	padding: 15px;
	margin: 30% 30%;
}
.close {
	color: rgb(104, 100, 100);
	float: right;
	font-size: 28px;
	font-weight: bold;
}
.close:hover,
.close:focus {
	color: black;
	text-decoration: none;
	cursor: pointer;
}
.task-card{
  transition: all 0.5s;
  display: inline-block;
  margin-right: 10px;
}
.list-complete-enter, .list-complete-leave-to
{
  opacity: 0;
  transform: translateY(30px);
}
.list-complete-leave-active {
  position: absolute;
}

p {
	color: whitesmoke;
}
</style>
