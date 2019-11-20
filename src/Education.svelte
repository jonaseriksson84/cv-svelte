<script>
  export let title;
  export let school;
  export let from;
  export let to;
  export let description;
</script>

<style type="text/scss">
  div {
    position: relative;
    margin-bottom: 60px;

    .fa-circle {
      position: absolute;
      left: -15px;
      top: 5px;
      font-size: 0.5rem;
      vertical-align: middle;
      margin-right: 15px;
    }

    strong.title {
      margin-bottom: 5px;
    }

    span {
      display: block;
    }

    em.dates {
      float: right;
    }

    li {
      margin-bottom: 5px;
      color: red !important;
    }
  }

  .divider {
    display: block;
    margin: 0 auto;
    background-color: #adadaf;
    height: 1px;
    width: 75%;
    margin-top: 25px;
  }
</style>

<div>
  <strong class="title">
    <i class="fa fa-circle" />
    {title}
  </strong>
  <em class="dates">{from} &mdash; {to}</em>
  <span>{school}</span>
  {#each description as desc}
    {@html desc}
  {/each}

</div>
