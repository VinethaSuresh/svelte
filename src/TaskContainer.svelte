<script>
  import List from "./List.svelte";
  import Controller from "./Controller.svelte";
   import uuid from "uuid/v1";
   export let listtype;
  let list = [];
  let isActive;
  function addItem(newItem) {
  list = [...list, { id: uuid(), task: newItem,deleted:false,completed:false }];
  console.log("list",list);
  }
   
  function removeItem(id)
  {
    let index;
   for(let i=0;i<list.length;i++)
   {
     if(list[i].id==id)
     {
       index=i;

     }
   }
   list[index].deleted=true;
   list=list;
   console.log(list);

  }
  function statusfinder(id)
  {
    
   for(let i=0;i<list.length;i++)
   {
     if(list[i].id==id)
     {
       
      list[i].completed = ! list[i].completed;
       
     }
   }
  }
</script>

<style>
  .taskContainer {
   
    width: 60%;
    margin-left: 400px;
  }
  .task {
    width: 80%;
    margin-left: 80px;
  }
  p{
    font-size: 30px;
    margin-left: 190px;
   
   
    font-family:Courier New, monospace;
    text-decoration: underline;
    text-decoration-color: red;
  }
</style>
<div class="taskContainer">
<p>Things TO DO</p>
  <div class="task">
    <Controller {addItem} />
    <List {list} {removeItem} {statusfinder} {listtype}/>
  </div>
</div>
