<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
	<link rel="shortcut icon" href="src/assets/favicon.ico" type="image/x-icon">
	<link href="https://fonts.googleapis.com/css?family=Ubuntu" rel="stylesheet">
	<title>Vue.js Todo</title>
</head>

<template>
  <div id="app">
	<TodoHeader></TodoHeader>
    <TodoInput></TodoInput>
    <TodoList></TodoList>
    <TodoFooter></TodoFooter> 
	</div>
</template>
 
<script>
import TodoHeader from './components/TodoHeader.vue'
import TodoFooter from './components/TodoFooter.vue'
import TodoInput from './components/TodoInput.vue'
import TodoList from './components/TodoList.vue'
	
	
export default {
	components: {
    'TodoHeader': TodoHeader,
    'TodoFooter': TodoFooter,
    'TodoInput': TodoInput,
    'TodoList': TodoList
  }

 
}
</script>
 
<style>
		body {
		text-align: center;
		background-color: #F6F6F8
	}
	input {
		border-style: groove;
		width: 200px;
	}
	button {
		border-style: groove;
	}
	.shadow {
		box-shadow: 5px 10px 10px rgba(0, 0, 0, 0.03)
	}
</style>