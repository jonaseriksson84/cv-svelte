<script>
  export let heading;
  export let words;
</script>

<style type="text/scss">

</style>

<p>
  <strong>{heading}:</strong>
  {words.join(', ')}
</p>
