<script>
import Title from './title.svelte';
import Navbar from "./navbar.svelte";
let newListsForApp = ['My expenses', 'Erease expenses'];
</script>


<Navbar titleApp="Budget Calculator" buttonAddItem="add item"/>
<!-- Each method -->
{#each newListsForApp as item}
    <Title title={item}/>    
{/each}



