<script>
  export let data = [];
</script>

<div class="timeline">
  {#each data as item}
  <div class="timeline__row">
    <p class="timeline__period">
      {item.from} &mdash; {item.to}
    </p>
    <div class="timeline__decor"></div>
    <div class="timeline__content">
      <h3 class="timeline__title">{item.title}</h3>
      <h6 class="timeline__subtitle">{item.subtitle}</h6>
      {#each item.text as text}
        <p class="timeline__text">{text}</p>
      {/each}
    </div>
  </div>
  {/each}
</div>

<style>
  .timeline {
    display: grid;
    row-gap: 2rem;
  }

  .timeline__row {
    display: grid;
    grid-template-columns: 20% min-content 1fr;
    column-gap: 1rem;
    align-items: baseline;
  }

  .timeline__period {
    margin-top: 0;
    margin-bottom: 0;
    font-style: italic;
    color: #666;
  }

  .timeline__decor {
    display: block;
    margin-top: 0.2em;
    width: 2.1rem;
    height: 2.1rem;
    box-shadow: inset 0 0 0 .7rem var(--accent-background);
  }

  .timeline__content {
    position: relative;
  }

  .timeline__title {
    margin-top: 0;
    margin-bottom: 0.2em;
    font-weight: 600;
    font-size: 2rem;
  }

  .timeline__subtitle {
    margin-top: 0;
    margin-bottom: 0.4em;
    font-weight: 500;
    font-size: 1.6rem;
  }

  .timeline__text {
    margin-top: 0;
    margin-bottom: 0.2em;
    font-weight: 400;
    font-size: 1.4rem;
  }

  .timeline__row:not(:last-child) .timeline__content::before {
    content: '';
    position: absolute;
    top: 2.1rem;
    left: -2.1rem;
    bottom: -2rem;
    width: .1rem;
    background-color: #666;
  }
</style>
