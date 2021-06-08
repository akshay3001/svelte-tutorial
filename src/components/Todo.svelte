<script>
  import { onMount } from "svelte";
  import { todos } from "../store/todo-store";

  onMount(async () => {
    const todoResponse = await fetch(
      "https://jsonplaceholder.typicode.com/todos"
    );
    const todo = await todoResponse.json();
    // console.log("Todo:", todo);
    return todos.update(() => {
      return [...todo];
    });
  });
</script>

<ul>
  {#each $todos as todo}
    <li>{todo.title}</li>
  {/each}
</ul>
