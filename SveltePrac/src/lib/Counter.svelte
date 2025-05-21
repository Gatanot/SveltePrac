<script>
  let count = 0; // 计数器初始值

  // 点击按钮时增加数字
  function increment() {
    count += 1;
  }
</script>

<div class="counter">
  <!-- 显示图片（替换为你的图片路径） -->
  <img
    src="https://via.placeholder.com/150" 
    alt="Counter Image"
    class="image"
  />

  <!-- 显示数字的按钮 -->
  <button on:click={increment} class="btn">
    Click Me: {count}
  </button>
</div>

<style>
  .counter {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    padding: 2rem;
    font-family: Arial, sans-serif;
  }

  .image {
    width: 150px;
    height: 150px;
    border-radius: 8px;
    object-fit: cover;
  }

  .btn {
    padding: 0.5rem 1rem;
    background: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 1rem;
    transition: background 0.3s;
  }

  .btn:hover {
    background: #45a049;
  }
</style>