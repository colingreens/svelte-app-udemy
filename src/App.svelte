<script>
  import TodoList from "./lib/TodoList.svelte";
  import { v4 as uuid } from "uuid";

  let todos = [
    {
      id: uuid(),
      title: "Todo 1",
      completed: true,
    },
    {
      id: uuid(),
      title: "Todo 2",
      completed: false,
    },
    {
      id: uuid(),
      title: "Todo 3",
      completed: true,
    },
  ];
  let todo = "";

  function handleAddTodo(event) {
    todo = event.detail.title;
  }
</script>

<h1>{todo}</h1>
<TodoList {todos} on:addtodo={handleAddTodo} />

<style>
</style>
