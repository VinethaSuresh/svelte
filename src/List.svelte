<script>
export let  list;
export let removeItem;
export let statusfinder;
import ListItem from "./ListItem.svelte";
  import TaskContainer from "./TaskContainer.svelte";
</script>

{#each list as listItem}
{#if ((listItem.deleted==false))}
<ListItem  {listItem} (listItem.id) { removeItem} {statusfinder}/>
{/if}
{/each}








