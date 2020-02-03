<script>
  let yes = false;

  export let listItem;

  function deletehandler() {
    let x = document.querySelector("p");
    x.remove();
  }
</script>

<style>

</style>
<p>
{#if yes}
 <strike><span>{listItem}</span> </strike>
{:else}
<span>{listItem}</span> 
{/if}
 
  <input type="checkbox" bind:checked={yes} />
  <span class="fa fa-trash w3-large" on:click={deletehandler} />
 </p>
