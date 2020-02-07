<script>
  import List from "./List.svelte";
  import Controller from "./Controller.svelte";
   import uuid from "uuid/v1";
  let list = [];
  
  function addItem(newItem) {
  list = [...list, { id: uuid(), task: newItem }];
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

  list.splice(index,1);
   list=list;
  return list;

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
    <List {list} {removeItem}/>
  </div>
</div>
