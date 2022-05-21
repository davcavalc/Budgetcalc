<script>
  //components
  import Navbar from "./navbar.svelte";
  import ExpensesList from "./ExpensesList.svelte";
  //data
  import expensesData from "./expenses";
  //variables
  let expenses = [...expensesData];
</script>

<Navbar />
<main class="content">
  <ExpensesList {expenses} />
</main>//TODO Parei na aula 19
