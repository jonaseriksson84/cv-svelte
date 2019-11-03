<script>
  import Buzzword from "./Buzzword.svelte";
  const src = "static/jonas-bw-size.png";

  const buzzwords = [
    {
      heading: "Frameworks",
      words: ["React", "AngularJS", "Django"]
    },
    {
      heading: "Languages",
      words: ["JavaScript", "Python", "Java", "SQL", "Jinja2"]
    },
    {
      heading: "Databases",
      words: ["postgres, MySQL"]
    },
    {
      heading: "Other",
      words: ["Amazon Web Services (AWS)", "Ansible", "Vagrant", "Jenkins"]
    }
  ];
</script>

<style type="text/scss">
  $color: #2f4f4f;

  /* RGB */
  $color1: rgba(230, 238, 214, 1);
  $color2: rgba(136, 149, 141, 1);
  $color3: rgba(96, 109, 93, 1);
  $color4: rgba(167, 38, 8, 1);
  $color5: rgba(9, 12, 2, 1);

  .cv {
    max-width: 1200px;
    margin: 100px auto;
    // background: url("static/ivory-paper.jpg");
    background-color: #e6e6e8;
    background-size: contain;
    box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
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

    aside {
      margin-left: 50px;
      padding: 0 40px;
      background-color: #dedee0;
      //box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
      border-right: 2px solid #ddd;
      max-width: 25%;
      padding-top: 50px;
      border-radius: 2px;
      z-index: 2;

      display: flex;
      flex-wrap: wrap;
      justify-content: center;

      .divider {
        display: block;
        margin: 0 auto;
        background-color: #4d4d4f;
        height: 3px;
        width: 75%;
        margin-top: 25px;
      }

      h2 {
        text-align: right;
        font-size: 1.25rem;
        letter-spacing: 0.1rem;
        margin-top: 50px;
      }

      .about p {
        text-align: justify;
      }

      .contact-block {
        text-align: right;
        width: 100%;

        .fa {
          width: 15px;
          margin-left: 15px;
          color: red;
          font-size: 1.25rem;
        }
      }
    }

    main {
      width: 75%;
      border-radius: 2px;
      z-index: 2;
    }

    h1 {
      color: $color2;
      display: block;
      font-size: 3rem;
      margin: 25px;
    }

    img {
      border-radius: 50%;
      width: 200px;
    }
  }
</style>

<div class="cv">

  <div class="background-element" />

  <aside>

    <img {src} alt="Jonas" />

    <div class="contact-block">
      <h2>CONTACT</h2>
      <p>
        070 420 01 75
        <i class="fa fa-phone" />
      </p>
      <p>
        Havsörnsvägen 85, 123 53 Farsta
        <i class="fa fa-map-marker" />
      </p>
      <p>
        jonaseriksson84@gmail.com
        <i class="fa fa-envelope" />
      </p>
      <p>
        www.mynameisjonas.dev
        <i class="fa fa-globe" />
      </p>
    </div>

    <div class="divider" />

    <div class="about">
      <h2>PROFILE</h2>
      <p>
        Jonas is a fullstack web developer with 7 years of professional
        experience. He particularly enjoys doing frontend development and
        JavaScript, though also comfortable with backend and API development.
      </p>
      <p>
        Jonas is a social person who thrives in a strong team, but he is also
        full of initiative and drive – and will quickly learn new processes,
        environments and technologies on his own. Regardless of project, Jonas
        always has a professional attitude and a clear focus on delivering
        results.
      </p>
    </div>

    <div class="divider" />

    <div class="buzzwords">
      <h2>SKILLS</h2>
      {#each buzzwords as buzzword}
        <Buzzword heading={buzzword.heading} words={buzzword.words} />
      {/each}
    </div>
  </aside>
  <main>
    <h2>Hi, my name is</h2>
    <h1>Jonas Eriksson</h1>
    <p>
      ... and I am a
      <strong>Fullstack Web Developer</strong>
    </p>
  </main>
</div>
