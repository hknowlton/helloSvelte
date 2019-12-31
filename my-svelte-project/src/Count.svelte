<script>
  let count = 0;
  $: doubled = count * 2;
  function handleClick() {
    count = count + 1;
  }
  $: if (count >= 10) {
    alert(`count is dangerously high!`);
    count = 9;
  }
</script>

<button on:click={handleClick}>
  Clicked {count} {count === 1 ? 'time' : 'times'}
</button>
<button on:click={() => (count = 0)}>Reset</button>
<br />
{#if count !== 0}{doubled} is double!{/if}
