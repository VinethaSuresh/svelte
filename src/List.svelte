<script>
export let  list;
export let removeItem;
export let statusfinder;
export let listtype;
import ListItem from "./ListItem.svelte";
import TaskContainer from "./TaskContainer.svelte";
</script>

{#each list as listItem (listItem.id)}
{#if (listtype=="all" && !listItem.deleted)}
  <ListItem  bind:listItem={listItem}  { removeItem} {statusfinder} />
{:else if (listtype=="active" && !listItem.completed && !listItem.deleted)}
<ListItem  bind:listItem={listItem} { removeItem} {statusfinder} />
{:else if (listtype=="completed" && listItem.completed && !listItem.deleted)}
<ListItem  bind:listItem={listItem} { removeItem} {statusfinder} />
{:else if (listtype=="deleted" &&  listItem.deleted)}
<ListItem  bind:listItem={listItem} { removeItem} {statusfinder} />
{/if}
{/each}








