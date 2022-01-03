<script lang="ts">
  let counter: number = 0;

  const modifyCounter = (value: number): number => (counter += value);
  const reset = (): number => (counter = 0);

  //   const add = (): number => counter++;

  //   const decrease = (): void => {
  //     counter--;
  //   };

  //   const reset = (): void => {
  //     counter = 0;
  //   };
</script>

<main>
  <h1>Counter App!</h1>
  <hr />
  <h2 class={counter < 0 ? "negative" : counter > 0 ? "positive" : "neutral"}>
    Counter: {counter}
  </h2>
  <button class="add" on:click={() => modifyCounter(1)}>+1</button>
  <button class="decrease" on:click={() => modifyCounter(-1)}>-1</button>
  <button class="reset" on:click={reset}>Reset</button>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    /*
	text-transform: uppercase;
	*/
    font-size: 4em;
    font-weight: 100;
  }

  h2 {
    font-size: 2rem;
  }

  .positive {
    color: olivedrab;
  }

  .negative {
    color: crimson;
  }

  .neutral {
    color: black;
  }

  button {
    font-size: 2rem;
    margin: 0 0.4rem;
    border-radius: 5px;
  }

  button:hover {
    cursor: pointer;
  }

  .add {
    background-color: #26d231;
  }

  .add:active {
    background-color: #19b623;
  }

  .decrease {
    background-color: #3a9aea;
  }

  .decrease:active {
    background-color: #1e6dad;
  }

  .reset {
    background-color: tomato;
  }

  .reset:active {
    background-color: #b64531;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
