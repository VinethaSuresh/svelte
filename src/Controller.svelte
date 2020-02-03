<script>
export let addItem;
let newItem="";
function clickhandler()
{
   
   addItem(newItem);
   newItem="";
    
}
function cancelhandler (){
  
   newItem="";

}
</script>

<input type="text" bind:value= {newItem}>
<button type="button" on:click={clickhandler}>Add task</button>
<button type="button" on:click= {cancelhandler}>Cancel</button>