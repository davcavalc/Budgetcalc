<script>
  import { setContext } from 'svelte';

  //components
  import Navbar from "./navbar.svelte";
  import ExpensesList from "./ExpensesList.svelte";
  //data
  import expensesData from "./expenses";
  //variables
  let expenses = [...expensesData];
  //functions
  function removeExpense(id) {
    expenses = expenses.filter(item => item.id !== id);
  }

  function deleteExpense(event) {
    const { id,name } = event.detail;
    console.log(name);
    removeExpense(id);
  }

  function clearExpenses(){
    expenses = [];
  }
  //context
  setContext("remove", removeExpense);
</script>

<Navbar />
<main class="content">
  <ExpensesList {expenses} on:delete={deleteExpense}/>
  <button type="button" class="btn btn-primary btn-block" on:click={clearExpenses}>
    clear expenses
  </button>
</main>

<!-- TODO parei na aula "Clear Expenses Button" -->