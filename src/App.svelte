<script lang="ts">
  import AutoComplete from "./components/AutoComplete/AutoComplete.svelte"
  import Menu from "./components/Menu/Menu.svelte";
  import Footer from "./components/Footer/Footer.svelte";

  // import { getAllFiles } from "./client/github"

  export let name: string;
  // export const gitignoreFiles = getAllFiles()
</script>

<style>
  /* Define Global Style */
  :global(body) {
    padding: 0;
  }

  /* App Components */
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }
  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<Menu />
<main>
  <h1>{name}</h1>
  <h2>Forever OpenSource</h2>
  <p>
    Templating the <code>.gitignore</code> for your liking.
  </p>
  <AutoComplete/>
</main>
<Footer />
