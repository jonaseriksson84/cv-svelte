<script>
  import Sidebar from "./Sidebar.svelte";
</script>

<style type="text/scss">
  .cv {
    max-width: 1200px;
    margin: 100px auto;
    // background: url("static/ivory-paper.jpg");
    background-color: #e6e6e8;
    background-size: contain;
    box-shadow: 0 19px 38px rgba(0, 0, 0, 0.3), 0 15px 12px rgba(0, 0, 0, 0.22);
    padding-top: 50px;
    display: flex;
    position: relative;
    z-index: 0;

    .background-element {
      background-color: #4d4d4f;
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 300px;
      z-index: 1;
    }

    main {
      width: 75%;
      border-radius: 2px;
      z-index: 2;
      padding: 50px;

      color: #e6e6e8;

      h1 {
        font-size: 5rem;
        margin: 0;
        text-align: center;
      }

      p {
        margin: 0;
        &:nth-of-type(2) {
          text-align: right;
        }
      }
    }
  }
</style>

<div class="cv">

  <div class="background-element" />

  <Sidebar />
  <main>
    <p>Hi, my name is</p>
    <h1>Jonas Eriksson</h1>
    <p>
      ... and I am a
      <strong>FULLSTACK WEB DEVELOPER</strong>
    </p>
  </main>
</div>
