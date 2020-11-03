<script>
  export let data = [];
</script>

<div class="summary">
  {#each data as item}
    <p class="summary__text">{item}</p>
  {/each}
</div>

<style>
  .summary__text {
    margin-top: 0;
    margin-bottom: 0;
    font-weight: 500;
    color: #555;
  }

  .summary__text:not(:first-of-type) {
    margin-top: 1em;
  }
</style>
