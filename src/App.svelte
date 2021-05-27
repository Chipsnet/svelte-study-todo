<script>
    let tasks = [];
    let newTodo = "";

    const remove = (i) => {
        tasks.splice(i, 1);
        tasks = tasks;
    };

    const add = () => {
        tasks.push(newTodo);
        tasks = tasks;
        newTodo = "";
    };
</script>

<main>
    <h1>Svelte-study-todo</h1>

    <input type="text" bind:value={newTodo} placeholder="ここにやることを入力してボタンをクリック" style="width: 400px;" />
    <button on:click={add}>追加</button>
    
    {#each tasks as t, i}
        <p on:click={() => remove(i)}>{t}</p>
    {/each}
</main>

<style>
</style>
