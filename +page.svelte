<script>
 let task = "";
 let taskList = [];
 function addHandler(){
    taskList = [...taskList, task];
 }
</script>

<h1>Welcome to SvelteKit</h1>
<input bind:value={task}/>
<button on:click={addHandler}>Pievienot</button>
<ul>
    {#each taskList as value}
        <li>{value}</li>
    {/each}
</ul>
<style>
    h1{
        color: green;
    }
</style>