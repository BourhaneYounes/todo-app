<script>
    import {addTodo} from "../stores/todoStore";
    let todo = '';
    const handleSubmit = () =>{
        addTodo(todo);
        todo = '';
        console.log("ok");
    }
</script>

<form class="my-10" on:submit|preventDefault={handleSubmit}>
    <div class="flex flex-col text-sm mb-2">
        <label for="todo" class="font-bold mb-2 text-gray-800">Todos</label>
        <input type="text" bind:value={todo} name="todo" placeholder="next task" class="appearance-none shadow border-gray-200
        p-2 focus:outline-none focus:border-gray-500 rounded-lg"/>
    </div>
    <button type="submit" class="w-full shadow-sm rounded text-sm p-1 bg-gray-200 hover:bg-gray-300 py-2 px-4">Submit</button>
</form>