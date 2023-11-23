<script>
  import Button from "./Button.svelte";
  import { createEventDispatcher } from "svelte";

  export let todos = [];
  let inputText = "";

  const dispatch = createEventDispatcher();

  function handleAddTodo() {
    dispatch("addtodo", {
      title: inputText,
    });
  }
</script>

<div class="todo-list-wrapper">
  <ul>
    {#each todos as { id, title }, index (id)}
      {@const number = index + 1}
      <li>{number}-{title}</li>
    {/each}
  </ul>
  <form class="add-todo-form" on:submit|preventDefault={handleAddTodo}>
    <input bind:value={inputText} />
    <Button type="submit" bgColor="red" disable={!inputText}>Add</Button>
  </form>
</div>
