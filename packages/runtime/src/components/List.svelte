<script>
  import Checker from './Checker.svelte'
  export let checkerResults
  export let ulStyle
  export let base
</script>

<ul style={ulStyle}>
  {#each checkerResults as checkerResult, index}
    <li>
      <Checker diagnostics={checkerResult.diagnostics} {base} {index} />
    </li>
  {/each}
</ul>

<style>
  ul,
  li {
    list-style: none;
  }
  ul {
    padding-inline: 0;
    margin-block: 0;
  }
</style>
