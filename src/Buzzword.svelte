<script>
  export let heading;
  export let words;
</script>

<style type="text/scss">
  p {
    margin-top: 0;
    margin-bottom: 10px;
    text-align: left;
  }
</style>

<p>
  <strong>{heading}:</strong>
  <br />
  {words.join(', ')}
</p>
