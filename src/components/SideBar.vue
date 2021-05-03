<template>
	<div>
		<img class ="user-image" v-bind:src="getImgUrl(username)">
		<h2>@{{username}}</h2>
		<ol >
			<l1><p>Profile</p></l1>
			<l1><p>ToDos</p></l1>
			<l1><p>Completed</p></l1>
			<l1><p>Urgent</p></l1>
			<l1><p>Groups</p></l1>
			
		</ol>
	</div>
</template>

<script>
export default {
	name : "SideBar",
	data : function(){
		return {
			username : 'moinak878',
		}
	},
	methods : {
		getImgUrl(pic) {
    		return require('../assets/'+pic+'.jpg')
		}
	}

};
</script>

<style scoped>
div {
	padding: 0px;
	background:linear-gradient(to bottom ,rgb(64, 97, 187),rgb(64,97,150));
	-webkit-flex: 1; /* Safari */
	-ms-flex: 1; /* IE 10 */
	flex: 1; /* Standard syntax */
	display: flex;
	flex-direction: column;
}
.user-image{
	display: block;
	border-radius: 50%;
	padding : auto;
	margin : 10px auto auto auto;
	height: 150px;
	width:150px;
}
h2 {
	flex: 1; /* Standard syntax */
	color: whitesmoke;
}
ol {
	flex: 1;
	display: flex;
	flex-direction: column;
	margin : auto 0 80% 0;
	padding : 10px 0px 0px 0px;

	background:  linear-gradient(to bottom ,rgb(87, 122, 161) , rgba(19, 36, 116, 0.2));
	
}
ol l1{
	/* padding: 10px auto 10px auto; */
	margin : 5px 0 0px 0;
	flex : 1;
	width : 100%;
	display: flex;
	flex-direction: row;
	height: 70%;

	
	
	
}
ol l1 p{
	flex :1 ;
	margin : 5px 5px ;
	box-shadow : 2px 5px 5px 2px rgba(19, 36, 116, 0.2);
	width : 80%;
	color : black;
}
</style>
