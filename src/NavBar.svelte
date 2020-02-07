<script>
export let navClickHandler;
</script><style>
  ul {
    list-style-type: none;
    padding: 0;
    line-height: 60px;
    font-size: 15px;
    font-weight: 10px;
    text-align: center;
    position: fixed;
    width: 20%;
    margin-top:120px;
  }

  li a {
    display: block;
    padding: 8px 16px;
    color: black;
  }
  li a:hover {
    text-decoration: underline;
    -webkit-text-decoration-color: red; /* Safari */
    text-decoration-color: red;
  }

</style>
<ul>
  <li>
    <a class="active" href="#all" id="all" on:click={navClickHandler}>All</a>
  </li>
  <li>
    <a href="#active" id = "active" on:click={navClickHandler}>Active</a>
  </li>
  <li>
    <a href="#completed" id="completed" on:click={navClickHandler}>Completed</a>
  </li>
  <li>
    <a href="#deleted" id="deleted" on:click={navClickHandler}>Deleted</a>
  </li>
</ul>

