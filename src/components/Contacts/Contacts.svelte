<script>
  export let data = [];
</script>

<div class="contacts">
  {#each data as item}
    <span class="contacts__title">
      {item.title}:
    </span>
    <span class="contacts__value">
      {item.value}
    </span>
  {/each}
</div>

<style>
  .contacts {
    display: grid;
    grid-template-columns: min-content 1fr;
    column-gap: 1rem;
    row-gap: .3rem;
  }

  .contacts__title {
    font-weight: 600;
    color: #333;
  }

  .contacts__value {
    font-weight: 500;
    color: #555;
  }
</style>
