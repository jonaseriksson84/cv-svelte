<script>
  export let title;
  export let company;
  export let from;
  export let to;
  export let description;
  export let words;
</script>

<style type="text/scss">
  div {
    padding-left: 25px;
    position: relative;
    margin-bottom: 50px;

    .fa-circle {
      position: absolute;
      left: -15px;
      top: 5px;
      font-size: 0.5rem;
      vertical-align: middle;
      margin-right: 15px;
    }

    strong.title {
      display: block;
      text-transform: uppercase;
      margin-bottom: 5px;
    }

    span.buzzwords {
      margin-top: 5px;
      display: block;
    }
  }
</style>

<div>
  <strong class="title">
    <i class="fa fa-circle" />
    {title}
  </strong>
  <span>{company} / {from} &mdash; {to}</span>
  <p>
    {description}
    {#if words}
      <span class="buzzwords">
        <strong>Methods & tools:</strong>
        <em>Bajs, Knark och Vapen</em>
      </span>
    {/if}
  </p>
</div>
