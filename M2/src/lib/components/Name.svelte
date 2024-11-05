<script>
  export let name = 'Henrik'; // En s.k. prop. 'Namn' = defaultvärde.
</script>
 

  
<input type="text" bind:value={name} /> 
<button on:click={() => name = 'Vadym'}>Mitt namn</button>
<p>Inskriven text: <strong>{name}</strong></p>

<style lang="scss">
  input {
       margin-bottom: 1rem;
   }
</style>
