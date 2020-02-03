<svelte:head>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css" />
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css" />

</svelte:head>

<script>
import uuid from 'uuid/v1'   
import List from "./List.svelte";
import Controller from "./Controller.svelte";
let list=[];
function addItem(newItem)
{
  
   list=[...list,{id:uuid(),task:newItem}]
   console.log("list",list);

}
</script>

<style>	

div{

  text-align:center;
}

h1{
  color:orangered;
}
</style>

<main>
<div>
<h1>To Do List</h1>
<Controller {addItem}/>
<List {list}/>
</div>
</main>
