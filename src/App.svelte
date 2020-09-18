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
  .myButton {
    background-color: white;
    color: black;
    border: 2px solid #f44336;
    padding: 16px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    transition-duration: 0.4s;
    cursor: pointer;
  }
  .myButton:hover {
    background-color: #f44336;
    color: white;
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
  <button on:click={handleClick} class="myButton">
    Clicked {count}
    {count === 1 ? 'time' : 'times'}
  </button>
</main>
