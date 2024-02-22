<script lang="ts">
  interface Todo {
    title: string;
    done: boolean;
  }
  let todoList: Todo[] = [];
  let titleCreate = "";

  function createTodo() {
    let newTodo: Todo = { title: titleCreate, done: false };
    todoList = [...todoList, newTodo];
    titleCreate = "";
    console.log(todoList);
  }
</script>

<h1>Welcome to Todo !</h1>

<h2>Todo Creation</h2>
<input
  type="text"
  name="title"
  placeholder="Todo title"
  bind:value={titleCreate}
/>
<button on:click={createTodo}>Create</button>
