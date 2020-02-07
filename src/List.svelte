<script>
export let  list;
export let removeItem;
import ListItem from "./ListItem.svelte";
  import TaskContainer from "./TaskContainer.svelte";
</script>

{#each list as listItem}
<ListItem  {listItem} (listItem.id) { removeItem}/>
{/each}








