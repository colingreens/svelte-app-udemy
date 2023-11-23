<script>
  export let initialCount; //required if no default value
  export let maxCount;

  let count = initialCount;
  
  $:string = `You have clicked ${count} times`

  function increment(){
    if (count === maxCount) {
      return;
    }
    count+= 1;
  }
</script>

<p>{string}</p>
<button on:click={increment}>Clicks {count}</button>

<style>
  button {
    padding: 15px 20px;
  }
</style>