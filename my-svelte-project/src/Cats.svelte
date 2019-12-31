<script>
  let cats = [
    { id: "J---aiyznGQ", name: "Keyboard Cat" },
    { id: "z_AbfPXTKms", name: "Maru" },
    { id: "OUtn3pvWmpg", name: "Henri The Existential Cat" }
  ];
</script>

<style>
  ul {
    width: 100px;
    margin: 0 auto;
  }
  h1 {
    color: #b12a90;
  }
</style>

<h1>The Famous Cats of YouTube</h1>

<ul>
  {#each cats as cat, i}
    <li>
      <a target="_blank" href="https://www.youtube.com/watch?v={cat.id}">
        {i + 1}: {cat.name}
      </a>
    </li>
  {/each}
</ul>
