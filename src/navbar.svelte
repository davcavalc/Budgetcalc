<script>
  export let titleApp;
  export let buttonAddItem;
</script>

<nav class="nav">
    <div class="nav-center">
      <h1 class="nav-title">{titleApp}</h1>
      <button type="button" class="nav-btn">
        <i class="far fa-plus-square">{buttonAddItem}</i>
      </button>
    </div>
  </nav>