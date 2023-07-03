<script>
  import Button from "../common/Button.svelte";
  import BookGrid from "./BookGrid.svelte";

  const books = [
    {
      id: 1,
      title: "Little Women",
      author: "Louisa May Alcott",
      cover: "",
      about: "Sisters learn to live in gratitude for each other.",
      variation: 0,
    },
    {
      id: 2,
      title: "Fahrenheit 451",
      author: "Ray Bradbury",
      cover: "",
      about:
        "Enter a dystopian future where books with ideas are dangerous, controlled and burned.",
      variation: 1,
    },
    {
      id: 3,
      title: "Grapes of Wrath",
      author: "John Steinbeck",
      cover: "",
      about:
        "Thousands set out from the dust bowl to California in search of better fortunes",
      variation: 2,
      favorite: true,
    },
    {
      id: 4,
      title: "To Kill a Mocking Bird",
      author: "Harper Lee",
      cover: "https://i.imgur.com/BPmn7bUm.jpg",
      about:
        "A girl learns to trust the wisdom of her father and not be dismayed by the prejudice around here.",
      variation: 0,
    },
    {
      id: 5,
      title: "Moby Dick",
      author: "Hermann Melville",
      cover: "",
      about:
        "Man hunts whale with a vengeance. In the end, he's the last man stand. I guess he won.",
      variation: 1,
    },
  ];
</script>

<header>
  <span class="preamble">Welcome to the</span>
  <h1>Library</h1>
</header>

<p class="greeting">
  This is a library for the people. Welcome. Read the books here. Be inspired.
  Go home and share them with your family.
</p>
<Button>+ Add Book</Button>
<BookGrid {books} />

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
