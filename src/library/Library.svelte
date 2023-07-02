<script>
    import Button from "../common/Button.svelte";
</script>

<header>
    <span class="preamble">Welcome to the</span><h1>Library</h1>
</header>

<p class="greeting">This is a library for the people. Welcome. Read the books here. Be inspired. Go home and share them with your family.</p>
<Button>+ Add Book</Button>
<style>
      header {
    margin: var(--spacingMedium) 0 var(--spacingLarge) 0;
    text-transform: uppercase;
  }
  .preamble {
    display: block;
  }
  h1 {
    font-size: var(--typeSizeXXLarge);
    font-weight: var(--typeWeightBold);
    line-height: var(--typeLineHeightTight);
  }

  .greeting {
    font-size: var(--typeSizeSmall);
  }

</style>