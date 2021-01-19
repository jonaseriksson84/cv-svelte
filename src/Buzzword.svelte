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
  @media print {
    p {
      width: calc(33% - 30px);
      margin: 15px;
    }
  }
</style>

<p class="buzz-word">
  <strong>{heading}:</strong>
  <br />
  {words.join(', ')}
</p>
