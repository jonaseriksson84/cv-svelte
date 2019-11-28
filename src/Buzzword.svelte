<script>
  export let heading;
  export let words;
</script>

<style type="text/scss">
  p {
    margin-top: 0;
    margin-bottom: 10px;
  }
</style>

<p>
  <strong>{heading}:</strong>
  {words.join(', ')}
</p>
