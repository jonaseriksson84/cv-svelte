<script>
  import Buzzword from "./Buzzword.svelte";
  const src = "static/jonas-bw-size.png";

  const buzzwords = [
    {
      heading: "Frameworks",
      words: ["React", "Svelte", "Vue", "AngularJS", "Django", "Node", "jQuery"]
    },
    {
      heading: "Languages",
      words: ["JavaScript", "Python", "HTML5", "CSS3", "Java", "SQL", "Jinja2"]
    },
    {
      heading: "Databases",
      words: ["postgres, MySQL, DB2"]
    },
    {
      heading: "Tooling",
      words: [
        "Webpack",
        "Rollup",
        "Gulp",
        "Grunt",
        "Yarn",
        "Karma",
        "Jasmine",
        "pytest"
      ]
    },
    {
      heading: "Version handling & CM",
      words: ["Git", "CVS", "SVN", "JIRA", "TFS"]
    },
    {
      heading: "Other",
      words: [
        "Amazon Web Services (AWS)",
        "Ansible",
        "Vagrant",
        "Jenkins",
        "Linux",
        "REST",
        "GraphQL",
        "Scrum",
        "Web Design",
        "Project Management"
      ]
    }
  ];
</script>

<style type="text/scss">
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

    img {
      border-radius: 50%;
      width: 200px;
    }

    .divider {
      display: block;
      margin: 0 auto;
      background-color: #4d4d4f;
      height: 2px;
      width: 75%;
      margin-top: 25px;
    }

    h3 {
      text-align: right;
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
</style>

<aside>

  <img {src} alt="Jonas" />

  <div class="contact-block">
    <h3>CONTACT</h3>
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
    <h3>PROFILE</h3>
    <p>
      Jonas is a fullstack web developer with 7 years of professional
      experience. He particularly enjoys doing frontend development and
      JavaScript, though also comfortable with backend and API development.
    </p>
    <p>
      Jonas is a social person who thrives in a strong team, but he is also full
      of initiative and drive – and will quickly learn new processes,
      environments and technologies on his own. Regardless of project, Jonas
      always has a professional attitude and a clear focus on delivering
      results.
    </p>
  </div>

  <div class="divider" />

  <div class="buzzwords">
    <h3>SKILLS</h3>
    {#each buzzwords as buzzword}
      <Buzzword heading={buzzword.heading} words={buzzword.words} />
    {/each}
  </div>
</aside>
