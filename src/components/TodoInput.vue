<<template>
    <div class="inputBox shadow">
		<input type="text" v-model="newTodoItem" placeholder="Type what you have to do"
			   v-on:keyup.enter="addTodo">
		<span class="addContainer" v-on:click="addTodo">
			<i class="addBtn fa fa-plus" aria-hidden="true"></i>
		</span>
	</div>
</template>
 
<<script>
export default {
	data() {
		return {
			newTodoItem: ''	
		}
	},
	methods: {
		addTodo() {
			  if (this.newTodoItem !== "") { // 1. 인풋박스의 입력 값이 있을때만 저장
				var value = this.newTodoItem && this.newTodoItem.trim(); // 인풋 박스에 입력된 텍스트의 앞뒤 공백 문자열 제거
				localStorage.setItem(value, value);
				this.clearInput(); // 3. 인풋 박스의 입력 값을 초기화
			}
		},
		clearInput() {
			this.newTodoItem = '';
		}
	}
}
</script>
<style>
	input:focus {
		outline: none;
	}
	.inputBox {
		background: white;
		height: 50px;
		line-height: 50px;
		border-radius: 5px;
	}
	.inputBox input {
		border-style:none;
		font-size: 0.9rem;
	}
	.addContainer {
		float: right;
		background: linear-gradient(to right, #6478FB, #8763FB);
		display: inline-block;
		width: 3rem;
		border-radius: 0 5px 5px 0;
	}
	.addBtn {
		color: white;
		vertical-align: middle
	}
	
	
</style>