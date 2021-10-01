<script lang="ts">
  import gsap from 'gsap'
  import { onMount } from 'svelte'
  export let headlineFirst: string
  export let headlineSecond: string
  export let biline: string

  onMount(() => {
    gsap.from(".container", { opacity: 0, y: -20, duration: 1 })
  })

</script>

<style lang="scss">
  .container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  .headline {
    display: flex;
    flex-direction: row;
    font-size: 18pt;

    .first {
      padding-right: 5pt;
      margin: 0 0 0 0;
    }

    .second {
      font-style: italic;
      margin: 0 0 0 0;
    }

  }

  .biline {
    margin: 0px 0px 0px 0px;
    font-weight: normal;
    font-size: 16pt;
  }

</style>

<div class="container">
  <div class="headline">
    <h1 class="first">{headlineFirst}</h1>
    <h1 class="second">{headlineSecond}</h1>
  </div>
  <h3 class="biline">{biline}</h3>
</div>
