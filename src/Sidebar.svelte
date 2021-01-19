<script>
  import Buzzword from "./Buzzword.svelte";

  const buzzwords = [
    {
      heading: "Frameworks",
      words: ["React", "Svelte", "AngularJS", "Django", "Node", "jQuery"]
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
      words: ["Git", "CVS", "SVN", "Confluence", "JIRA", "TFS"]
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
    @media screen and (min-width: 500px) {
      max-width: 25%;
    }
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
      text-align: left;
      width: 100%;

      .fa {
        width: 15px;
        margin-right: 5px;
        color: red;
        font-size: 1.25rem;
      }
    }

    @media print {
      .language {
        display: none;
      }
      .buzzwords {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
      }

      .contact-block {
        text-align: center;
        p {
          display: block;
        }
      }

      h2 {
        text-align: left;
      }

      div.block-thing {
        flex: 0 50%;
      }
    }
  }
</style>

<aside>
  <div class="contact-block">

    <p>
      <i class="fa fa-phone" />
      070 420 01 75
    </p>
    <p>
      <i class="fa fa-map-marker" />
      Havsörnsvägen 85, 123 53 Farsta
    </p>
    <p>
      <i class="fa fa-envelope" />
      jonaseriksson84@gmail.com
    </p>
    <p>
      <i class="fa fa-globe" />
      www.mynameisjonas.dev
    </p>
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
