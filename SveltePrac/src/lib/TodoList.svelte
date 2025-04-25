<script>
    // 定义组件的props
    export let todos = [];
  
    // 删除待办事项的函数
    function removeTodo(index) {
      todos = todos.filter((_, i) => i !== index);
    }
  </script>
  
  <div class="todo-list">
    <h2>待办事项</h2>
    
    {#if todos.length === 0}
      <p>暂无待办事项</p>
    {:else}
      <ul>
        {#each todos as todo, index (index)}
          <li>
            {todo}
            <button on:click={() => removeTodo(index)}>删除</button>
          </li>
        {/each}
      </ul>
    {/if}
  </div>
  
  <style>
    .todo-list {
      max-width: 400px;
      margin: 0 auto;
      padding: 20px;
      border: 1px solid #ddd;
      border-radius: 8px;
      font-family: Arial, sans-serif;
    }
    
    h2 {
      margin-top: 0;
      color: #333;
    }
    
    ul {
      list-style: none;
      padding: 0;
    }
    
    li {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 8px 0;
      border-bottom: 1px solid #eee;
    }
    
    button {
      background-color: #ff4444;
      color: white;
      border: none;
      padding: 5px 10px;
      border-radius: 4px;
      cursor: pointer;
    }
    
    button:hover {
      background-color: #cc0000;
    }
  </style>