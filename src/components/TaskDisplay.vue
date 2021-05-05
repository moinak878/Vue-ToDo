<template>
	<!-- display all tasks here  -->
	<div class="container">
		<div class="main-area">
			<div class="task-card" v-for="task in tasks" v-bind:key="task.id">
				<img src="../assets/logo.png" />
				<p>{{ task.msg }}</p>
			</div>
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
					id: 1,
					msg: "This is sample task 1 that i have to complete by 1/1/2021",
				},
				{
					id: 1,
					msg: "This is sample task 1 that i have to complete by 1/1/2021",
				},
				{
					id: 1,
					msg: "This is sample task 1 that i have to complete by 1/1/2021",
				},
				{
					id: 1,
					msg: "This is sample task 1 that i have to complete by 1/1/2021",
				},
			],
		};
	},
	methods: {
		AddTask: function() {
			console.log("click me!");
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
p {
	color: whitesmoke;
}
</style>
