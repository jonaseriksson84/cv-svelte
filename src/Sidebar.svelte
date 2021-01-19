<script>
  import Buzzword from "./Buzzword.svelte";

  const buzzwords = [
    {
      heading: "Frameworks",
      words: ["React", "Svelte", "AngularJS", "Django", "Node"]
    },
    {
      heading: "Languages",
      words: ["JavaScript", "Python", "HTML5", "CSS3", "Java", "SQL", "Jinja2"]
    },
    {
      heading: "Databases",
      words: ["postgres", "MySQL", "DB2"]
    },
    {
      heading: "Tooling",
      words: [
        "Grunt",
        "Gulp",
        "Jasmine",
        "Karma",
        "npm",
        "pytest",
        "Rollup",
        "Webpack",
        "Yarn"
      ]
    },
    {
      heading: "Version handling & CM",
      words: ["Git", "CVS", "SVN", "Confluence", "JIRA"]
    },
    {
      heading: "Other",
      words: [
        "AWS",
        "Ansible",
        "Docker",
        "Jenkins",
        "Linux",
        "REST",
        "Scrum",
        "Vagrant"
      ]
    }
  ];
</script>

<style type="text/scss">
  aside {
    max-width: 25%;
    padding: 0 15px;

    .divider {
      display: block;
      margin: 0 auto;
      background-color: #4d4d4f;
      height: 2px;
      width: 100%;
      margin: 25px 0;
    }

    h2 {
      text-align: left;
    }

    .about p {
      text-align: justify;
    }

    .contact-block {
      display: flex;
      flex-direction: column;
      align-items: start;

      .icon {
        margin-top: 20px;
        display: flex;

        span {
          display: block;
        }
      }

      .fa {
        width: 40px;
        text-align: center;
        color: red;
        font-size: 1.25rem;
      }
    }
  }
</style>

<aside>
  <div class="contact-block">
    <div class="icon">
      <i class="fa fa-phone" />
      <div>070 420 01 75</div>
    </div>
    <div class="icon">
      <i class="fa fa-envelope" />
      jonaseriksson84@gmail.com
    </div>
    <div class="icon">
      <i class="fa fa-map-marker" />
      <div>
        <span>Bryggvägen 6B</span>
        <span>117 71 Stockholm</span>
      </div>
    </div>
    <div class="icon">
      <i class="fa fa-globe" />
      www.mynameisjonas.dev
    </div>
  </div>

  <div class="divider" />

  <div class="about">
    <p>
      I am a fullstack web developer with 8+ years of professional experience. I
      particularly enjoy doing frontend development and JavaScript, though also
      comfortable with backend and API development in a number of languages such
      as Python, Java and server-side JavaScript.
    </p>
    <p>
      I am a social person and thrive in a strong team, but I am also full of
      initiative and drive – I will quickly learn new processes, environments
      and technologies on my own. Regardless of project, I always carry a
      professional attitude and clear focus on delivering results.
    </p>
  </div>

  <div class="divider" />

  <div class="buzzwords">
    {#each buzzwords as buzzword}
      <Buzzword heading={buzzword.heading} words={buzzword.words} />
    {/each}
  </div>
  <div class="divider" />
  <div class="language">
    <strong>Swedish:</strong>
    Native
    <br />
    <strong>English:</strong>
    Fluent
    <br />
    <strong>German:</strong>
    Basic proficiency
    <br />
    <strong>Italian</strong>
    Basic proficiency
    <br />
    <strong>Japanese:</strong>
    Basic proficiency
  </div>
</aside>
