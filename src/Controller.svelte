<script>
  export let addItem;
  let newItem = "";
  let emptyAdded = false;
  let addTask=false;
  function clickhandler() {
    addToList();
  }

  function keyuphandler(event)
  {
    if(event.keyCode===13)
    {
      event.preventDefault();
      addToList();
    }
  }

  function addToList(){
    if (newItem != "") {
      emptyAdded = false;
      addItem(newItem);
      newItem = "";
    } else {
      emptyAdded = true;
    }
  }

  function cancelhandler() {
    newItem = "";
  }

  function myFunction() {
    emptyAdded = false;
  }



</script>
<style>
input{
    width:350px;

  }
  p{
    color:red;
  }

  button:hover{
    border:2px solid skyblue;
  }
 div{
   margin-bottom:15px;
 }
</style>
<div>
<input type="text" bind:value={newItem} placeholder="add a new to do" on:input={myFunction}  on:keyup={keyuphandler} maxlength="40" />
<button type="button" on:click={clickhandler}>Add</button>
<button type="button" on:click={cancelhandler}>Clear</button>
</div>
{#if emptyAdded}
  <p>Please Enter Task</p>
{/if}
