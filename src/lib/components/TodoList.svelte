<script>
    let todos = $state([
        { title: "<i>Assignment 1</i>", done: false },
        { title: "<b>Assignment 2</b>", done: false }, 
        { title: "Assignment 3", done: false },
    ]);
</script>

{#snippet todoItem(todo)} <!--come deve essere renderizzato un singolo todo-->
        <li>
        <label>
            <input type="checkbox" bind:checked={todo.done}>
            {@html todo.title} {todo.done ? '✅' : '❌'}
            </label>
        </li>
        {/snippet}
        
<h3> My Todos</h3>

<ul>
    {#each todos as todo} 
    {@render todoItem(todo)}
       <!-- <li>-->
          <!--  <input type="checkbox" bind:checked={todo.done}>-->
           <!-- {todo.title} {todo.done ? '✅' : '❌'}-->
       <!-- </li> Tutta questa parte la uso quando non ho il render perchè non ho lo snippet-->
    {/each}
</ul>

<style>
    label :global {
        i{ color: green;}
        b {
            color:blue;
        }    }
</style>