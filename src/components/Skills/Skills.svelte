<script>
  export let data = []
</script>

<div class="skills">
  {#each data as item}
    <div class="skills__column">
      <h5 class="skills__title">
        {item.title}
      </h5>
      {#each item.text as text}
        <p class="skills__value">
          {text}
        </p>
      {/each}
    </div>
  {/each}
</div>


<style>
  .skills {
    display: flex;
    flex-wrap: wrap;
    margin-left: -1rem;
    margin-right: -1rem;
  }

  .skills__column {
    padding-left: 1rem;
    padding-right: 1rem;
    min-width: calc(25% - 2rem);
    flex: 1 1 0;
  }

  .skills__title {
    display: inline-flex;
    padding: .2em .5em;
    margin-bottom: 1em;
    margin-top: 0;
    background-color: var(--accent-background);
    font-weight: 600;
    font-size: 1.8rem;
    color: var(--accent-color);
  }

  .skills__value {
    display: flex;
    align-items: start;
    padding-top: .2em;
    padding-bottom: .2em;
    margin-top: 0;
    margin-bottom: 0;
    font-weight: 600;
    font-size: 1.6rem;
    color: #666;
  }

  .skills__value::before {
    flex-shrink: 0;
    content: '';
    margin-top: 0.5em;
    margin-right: 0.5em;
    width: .4em;
    height: .4em;
    border-radius: 50%;
    background-color: var(--accent-background);
  }

  .skills__value:not(:first-of-type) {
    margin-top: 0.2em;
  }
</style>
