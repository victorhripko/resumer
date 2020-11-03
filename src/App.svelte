<script>
  import Header from './components/Header/Header.svelte';
  import Contacts from './components/Contacts/Contacts.svelte';
  import Summary from './components/Summary/Summary.svelte';
  import Timeline from './components/Timeline/Timeline.svelte';
  import Skills from './components/Skills/Skills.svelte';

  import data from './data.json';
</script>

<div class="page"
  style="
    --accent-background: {data.background};
    --accent-color: {data.color};
  ">
  <Header
    firstName={data.firstName}
    lastName={data.lastName}
  />

  {#if data.contacts}
    <Contacts data={data.contacts} />
  {/if}

  {#if data.summary}
    <h5 class="page__title">
      {data.summary.title}
    </h5>

    <Summary data={data.summary.text} />
  {/if}

  {#if data.timelines}
    {#each data.timelines as timeline}
      <h5 class="page__title">
        {timeline.title}
      </h5>

      <Timeline data={timeline.content} />
    {/each}
  {/if}

  {#if data.skills}
    <h5 class="page__title">
      {data.skills.title}
    </h5>
    <Skills data={data.skills.content} />
  {/if}

</div>


<style>
  .page {
    --accent-background: #563eff;
    --accent-color: white;

    padding-bottom: 15mm;
    display: grid;
    row-gap: 2rem;
    max-width: 1200px;
    margin-left: auto;
    margin-right: auto;
    padding-left: 1.5rem;
    padding-right: 1.5rem;
  }

  .page__title {
    text-transform: uppercase;
    font-size: 2.4rem;
    background-image: linear-gradient(var(--accent-background), var(--accent-background));
    background-repeat: no-repeat;
    background-size: 1.5em .1em;
    background-position: left bottom;
  }
</style>
