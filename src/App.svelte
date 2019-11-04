<script>
  import Sidebar from "./Sidebar.svelte";
  import Experience from "./Experience.svelte";

  const experiences = [
    {
      title: "FULLSTACK WEB DEVELOPER",
      company: "Reason Studios",
      from: "October 2017",
      to: "present",
      description: ["Bla bla bla"],
      words: ["Bajs", "Knark", "Vapen"]
    },
    {
      title: "CONSULTANT",
      company: "HiQ",
      from: "August 2014",
      to: "October 2017",
      description: [
        "<p>Worked as a consultant in primarily frontend positions in the organizations listed below.</p>"
      ]
    },
    {
      title: "FULLSTACK DEVELOPER",
      company: "Swedish Police",
      from: "June 2016",
      to: "October 2017",
      description: [
        "<p>Jonas was the lead frontend developer for internal tools ported from COBOL systems to modern web-based applications. In addition to frontend development Jonas has also done significant backend development.",
        "<ul><li>Delivered two applications into production far ahead of schedule</li><li>Introduced frontend build systems and frontend testing into the team.</li></ul>"
      ],
      words: [
        "AngularJS",
        "JavaScript",
        "HTML5",
        "CSS3",
        "LESS",
        "Java 1.8",
        "JBoss 6.4",
        "Git",
        "REST",
        "Swagger",
        "Gulp",
        "Karma",
        "Jasmine",
        "Maven"
      ]
    },
    {
      title: "FRONTEND DEVELOPER",
      company: "Midroc",
      from: "October 2014",
      to: "June 2016",
      description: [
        "<p>For the most part Jonas worked as solo or primary front end developer. In addition to implementation, Jonas has also had extensive input on UX elements and design. Moreover, Jonas has been responsible for introducting many new APIs and technologies such as the Sharepoint API, Microsoft ADAL.js and Microsoft Graph API to the organization.</p>",
        "<ul><li>New Intranet based on Sharepoint REST API and AngularJS frontend. Starting point for 1 100 employees and 70 000 visits per month.</li><li>Campaign portal celebrating the client's 20-year anniversary.</li><li>Modern responsive portals for project reporting used by in-field technicians and PMs/administrators.</li><li>Performance and UX improvements for time reporting portal.</li></ul>"
      ],
      words: [
        "AngularJS",
        "Azure AD",
        "Bower",
        "CAML",
        "CSS3",
        "Git",
        "Git-TF",
        "GruntJS",
        "HTML5",
        "Jasmine",
        "JavaScript",
        "jQuery",
        "Karma",
        "LESS",
        "Microsoft ADAL.js",
        "Microsoft Graph API",
        "Node",
        "npm",
        "OAuth2",
        "REST",
        "SASS",
        "SCRUM",
        "Sharepoint Online",
        "Sharepoint REST API",
        "TFS",
        "Yammer",
        "Yeoman"
      ]
    }
  ];
</script>

<style type="text/scss">
  .cv {
    @media screen {
      max-width: 1200px;
      margin: 100px auto;
      background-color: #e6e6e8;
      background-size: contain;
      box-shadow: 0 19px 38px rgba(0, 0, 0, 0.3),
        0 15px 12px rgba(0, 0, 0, 0.22);
      padding-top: 50px;
    }
    // background: url("static/ivory-paper.jpg");
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

      .name {
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

      h3 {
        margin-top: 90px;
      }
    }
  }
</style>

<div class="cv">

  <div class="background-element" />

  <Sidebar />
  <main>
    <div class="name">
      <p>Hi, my name is</p>
      <h1>Jonas Eriksson</h1>
      <p>
        ... and I am a
        <strong>FULLSTACK WEB DEVELOPER</strong>
      </p>
    </div>
    <h3>EXPERIENCE</h3>

    {#each experiences as exp}
      <Experience
        title={exp.title}
        company={exp.company}
        from={exp.from}
        to={exp.to}
        description={exp.description}
        words={exp.words} />
    {/each}
  </main>
</div>
