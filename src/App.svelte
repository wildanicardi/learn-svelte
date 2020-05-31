<script>
  import EmojiComponent from "./EmojiComponent.svelte";
  let isLoading = false;
  let currentEmoji = "😂";
  setTimeout(function() {
    isLoading = true;
  }, 2500);
</script>

<style>
  /* main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  } */
  div {
    margin: 2em;
  }
  button {
    background-color: #8bd3dd;
    padding: 0.75em;
    border-radius: 0.25em;
    border: 2px solid #000;
    box-shadow: 0.4rem 0.4rem 0 #222;
  }
  button:hover {
    box-shadow: 0.25rem 0.25rem 0 #222;
    transition: all 0.4s ease 0s;
    background-color: #8bd;
  }
  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 2em;
    font-weight: 20;
  }

  /* @media (min-width: 640px) {
    main {
      max-width: none;
    }
  } */
</style>

<div>
  <h1>Randomize Emoji</h1>
  {#if isLoading === true}
    <EmojiComponent {currentEmoji} />
    <button>Randomize</button>
  {:else}
    <h2>Loading....</h2>
  {/if}

</div>
