<script>
  export let heading;
  export let words;
</script>

<style type="text/scss">
  p {
    margin-top: 0;
    margin-bottom: 10px;
    text-align: center;
  }
</style>

<p>
  <strong>{heading}:</strong>
  {#each words as word, i}
    <br />
    {word}
  {/each}
</p>
