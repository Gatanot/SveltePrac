<script>
  import svelteLogo from "./assets/svelte.svg";
  import viteLogo from "/vite.svg";
  import Counter from "./lib/Counter.svelte";
  import TimePanel from "./lib/TimePanel.svelte";
  import TodoList from "./lib/TodoList.svelte";
  const TargetTime=new Date()
  let Todos=["人工智能实验报告","信号与系统实验报告","软件工程策划案"]
</script>

<main>
  <h1>Git + Svelte 练习</h1>
  <h2>Counter</h2>
  <Counter />
  <h2>TimePanel</h2>
  <TimePanel {TargetTime}/>
  <h2>TodoList</h2>
  <TodoList {Todos}/>
</main>

<style>
</style>
