<script>
  let yes = false;
  export let removeItem;
  export let listItem;
  export let statusfinder;

  function deletehandler() {
   removeItem(listItem.id); 
  }
  function checkboxhandler()
  {
    statusfinder(listItem.id);
  }


</script>

<style>

strike
{
  color:red;
}
.itemsContainer{
  
  width:500px;
  background-color:white;
  border-bottom:1pt groove gray;
  border-top:1pt groove gray; 
  border-left:1pt groove gray;
  border-right:1pt groove gray; 
  display: flex;
  flex-direction: row;
  height:35px;
  margin:0px 0px;
}

.itemsContainer:hover{

  background-color:lightgray;
}
.textContainer
{

  font-size:18px;
  font-weight:15px;
  font-family:Arial, Helvetica, sans-serif;
  line-height:5px;
  margin-top:15px;
  margin-bottom:10px;
  width:460px;
}

.text
{
  padding-top:15px;
   padding-bottom:10px;
   padding-left:10px; 
}
.CheckboxContainer
{
  width:20px;
  margin-top:8px;
 
}
.deleteContainer
{
width:20px; 
}
.deleteclass
{
  padding-top:8px;
  padding-bottom:9px;
  padding-left:0px;
}
strike
{
   padding-top:15px;
   padding-bottom:10px;
}

.checkbox
{
  margin-left:5px;
}
</style>

<div class="itemsContainer">
<div class="CheckboxContainer">
 <input type="checkbox" checked={listItem.completed} class="checkbox" on:click={checkboxhandler}/>
 </div>
 <div class="textContainer">
{#if listItem.completed}
 <strike><span class="text">{listItem.task}</span> </strike>
{:else}
<span class="text">{listItem.task}</span> 
{/if}
 </div>
 <div class="deleteContainer">
 <span class="fa fa-trash w3-large deleteclass" on:click={deletehandler} />
 </div>
 </div>
