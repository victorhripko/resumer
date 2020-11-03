<script>
  export let firstName = 'John';
  export let lastName = 'Doe';
</script>

<header class="header">
  <span class="hello">Hello.</span>
  <h1 class="title">
    My name is {firstName}&nbsp;{lastName}, <br />
    and this is <strike class="strike">my resume<span class="strike__story">my story</span></strike>
  </h1>
</header>

<style>
  .hello {
    display: inline-block;
    background-color: var(--accent-background);
    color: var(--accent-color);
    font-size: 2rem;
    font-weight: 500;
    padding: 1.5em .7em .5em;
  }

  .title {
    font-size: 4.2rem;
    font-weight: 700;
    padding-bottom: 0.25em;
  }

  .strike {
    position: relative;
  }

  .strike__story {
    position: absolute;
    top: 70%;
    left: 30%;
    white-space: nowrap;
    background-color: var(--accent-background);
    color: var(--accent-color);
    line-height: 1.1;
    padding: .05em .2em .2em;
  }
</style>
