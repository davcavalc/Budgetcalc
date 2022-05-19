<script>
import Title from './title.svelte';
import Navbar from "./navbar.svelte";
let myFruits = ['apple', 'orange', 'lemon'];
</script>


<Navbar titleApp="Budget Calculator" buttonAddItem="add item"/>
<!-- Each method -->
{#each myFruits as item}
    <Title title={item}/>    
{/each}



