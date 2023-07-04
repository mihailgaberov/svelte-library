<script>
    import BackButtonRow from "../common/BackButtonRow.svelte";
    import BookCover from "../common/BookCover.svelte";
    import Button from "../common/Button.svelte";
    import Header from "../common/Header.svelte";
    import { httpPost } from "../common/api.js";
    import TextInput from "./TextInput.svelte";

    let title = '';

    function handleInput(event) {
        title = event.target.value
    }

    $: console.log({title})
  </script>
  
  <BackButtonRow />
  
  <Header element="h1" size="large">Create</Header>
  
  <form>
    <div class="fields">
        <TextInput label="Title" bind:value={title} />
    </div>
  
    <div>
      <Header>Preview</Header>
      <div class="preview">
      </div>
    </div>
  </form>
  
  <style>
    form {
      display: grid;
      grid-auto-rows: auto;
      grid-template-columns: 1fr;
      gap: var(--spacingXLarge);
    }
    .fields {
      display: grid;
      grid-auto-rows: auto;
      gap: var(--spacingMedium);
    }
    .preview {
      display: grid;
      grid-template-columns: minmax(20vw, 10rem);
      grid-template-rows: minmax(32vw, 16rem);
    }
    @media (min-width: 48rem) {
      form {
        grid-template-columns: 60vw 20vw;
      }
    }
  </style>
  