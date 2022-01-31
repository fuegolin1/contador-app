<script lang="ts">
  let counter: number = 0;

  const modifyCounter = (value: number): number => (counter += value);
  const reset = (): number => (counter = 0);

  //   const add = (): void => {
  //     counter++;
  //   };

  //   const rest = (): void => {
  //     counter--;
  //   };
  //   const resect = (): void => {
  //     counter = 0;
  //   };
</script>

<main>
  <h1>Contador app</h1>
  <h2 class={counter < 0 ? "negative" : "positive"}>contador: {counter}</h2>

  <button class="btn btn-primary" on:click={() => modifyCounter(1)}
    >Contar + 1</button
  >
  <button class="btn btn-warning" on:click={() => modifyCounter(-1)}
    >Contar - 1</button
  >
  <button class="btn btn-danger" on:click={reset}>Reset</button>
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
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  .negative {
    color: #ff3e00;
  }
  .positive {
    color: rgb(44, 109, 6);
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
