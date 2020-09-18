<script>
  export let name;

  let count = 0;
  function handleClick() {
    count += 1;
  }
</script>

<style>
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
    font-family: "Comic Sans MS", cursive;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <h1>Hello {name}!</h1>
  <p>My first application using svelte. &#128526</p>
  <button on:click={handleClick}>
    Clicked {count}
    {count === 1 ? 'time' : 'times'}
  </button>
</main>
