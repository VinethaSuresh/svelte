<script>
export let  list;
import ListItem from "./ListItem.svelte";
</script>

{#each list as listItem}
<ListItem  listItem={listItem.task} (listItem.id)/>
{/each}








