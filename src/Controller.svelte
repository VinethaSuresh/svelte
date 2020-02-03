<script>
export let addItem;
let newItem="";
let emptyAdded = false;
function clickhandler()
{ 
   if (newItem !=""){
      emptyAdded=false;
      addItem(newItem);
      newItem="";  
   }
   else{
      emptyAdded=true;
   }

}
    

function cancelhandler (){
  
   newItem="";

}
</script>
<input type="text" bind:value={newItem} placeholder="Add Task"/>
<button type="button" on:click={clickhandler} >Add Task</button>
<button type="button" on:click= {cancelhandler}>Cancel</button>
{#if emptyAdded}
<p>please enter text</p>
{/if}