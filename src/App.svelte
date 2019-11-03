<script>
  import Buzzword from "./Buzzword.svelte";
  const src = "static/jonas-bw.png";

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

  .header {
    padding: 50px 15px;
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    background: url("static/ivory-paper.jpg");
    background-size: contain;
    h1 {
      color: $color2;
      display: block;
      font-size: 3rem;
      margin: 25px;
    }

    img {
      border-radius: 50%;
      width: 150px;
      border: 12px solid $color2;
    }

    .contact-block {
      display: flex;
      text-align: center;
      justify-content: space-around;

      div {
        min-width: 210px;

        span,
        strong {
          display: block;
        }

        strong {
          color: $color2;
        }
      }
    }

    .about,
    .buzzwords {
      width: 100%;
      margin: 25px 0;
      padding: 15px;
      border: 1px solid #ddd;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
      transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);

      &:hover {
        box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25),
          0 10px 10px rgba(0, 0, 0, 0.22);
      }

      h2 {
        text-align: center;
      }
    }
  }
</style>

<div class="header">

  <img {src} alt="Jonas" />

  <h1>Jonas Eriksson</h1>

  <div class="contact-block">

    <div>
      <strong>Phone Number</strong>
      070 420 01 75
    </div>

    <div>
      <strong>Address</strong>
      <span>Havsörnsvägen 85</span>
      123 53 Farsta
    </div>

    <div>
      <strong>Email</strong>
      jonaseriksson84@gmail.com
    </div>

    <div>
      <strong>Website</strong>
      mynameisjonas.code
    </div>

  </div>

  <div class="about">
    <h2>About Jonas</h2>
    <p>
      Jonas is a frontend developer with a passion for the latest web technology
      who takes satisfaction in rapid delivery of modern applications providing
      tangible customer satisfaction. Jonas is an accomplished software engineer
      who enjoys taking responsibility for software architecture. He has
      previously also worked as a fullstack Java developer.
    </p>
    <p>
      Jonas is a social person who enjoys being part of a strong team, but is
      also full of initiative and drive – and will quickly learn new processes,
      environments and systems on his own.
    </p>
    <p>
      Experiences from outsourcing organizations and international exchange
      studies have shown him competent even in strongly heterogeneous
      organizations. Regardless of project, Jonas always shows a professional
      attitude and a clear focus on delivering results.
    </p>
  </div>

  <div class="buzzwords">
    <h2>Buzzwords</h2>
    {#each buzzwords as buzzword}
      <Buzzword heading={buzzword.heading} words={buzzword.words} />
    {/each}
  </div>

  <h1>TJA</h1>
  <p>BAJS BAJS BAJS</p>
</div>
