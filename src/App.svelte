<script>

  import TitleBar from "./TitleBar.svelte";
  import NavBar from "./NavBar.svelte";
  import TaskContainer from "./TaskContainer.svelte";
   
</script>

<style>
  :global(body) {
    padding: 0px 0px;
    background-color: #f1f1f1;
    scroll-behavior: smooth;
  }
</style>

<svelte:head>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css" />
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css" />

</svelte:head>
<main>
  <TitleBar />
  <NavBar />
  <TaskContainer />
</main>
