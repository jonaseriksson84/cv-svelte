<script>
  import Sidebar from "./Sidebar.svelte";
  import Experience from "./Experience.svelte";
  import Education from "./Education.svelte";

  const src = "static/jonas-bw-size.png";

  const experiences = [
    {
      title: "FULLSTACK WEB DEVELOPER",
      company: "Reason Studios",
      from: "October 2017",
      to: "present",
      description: [
        "<p>I currently work as a the lead fullstack web developer in the Sales & Marcom department of Reason Studios (formerly Propellerhead Software)</p>",
        "<ul><li>Quickly got up to speed in new languages for the position - Python & Django.</li><li>Technical responsibility for web shop generating 75% of the yearly $120M revenue</li><li>True full stack development all the way from database to React frontend.</li><li>Extensively involved in infrastructure and devops.</li></ul>"
      ],
      words: [
        "React",
        "Django",
        "jQuery",
        "JavaScript",
        "Python",
        "HTML5",
        "CSS3",
        "SCSS",
        "Java",
        "SQL",
        "Jinja2",
        "postgres",
        "MySQL",
        "Webpack",
        "pytest",
        "Git",
        "JIRA",
        "AWS",
        "Ansible",
        "Vagrant",
        "Jenkins",
        "Linux",
        "REST"
      ]
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
        "<p>I was the lead frontend developer for internal tools ported from COBOL systems to modern web-based applications. In addition to frontend development I also did significant backend development.",
        "<ul><li>Delivered two applications into production far ahead of schedule</li><li>Introduced frontend build systems and frontend testing into the team.</li></ul>"
      ],
      words: [
        "AngularJS",
        "JavaScript",
        "HTML5",
        "CSS3",
        "LESS",
        "Java",
        "JBoss",
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
        "<p>For the most part I worked as solo or primary front end developer. In addition to implementation, I also had extensive input on UX elements and design. Moreover, I was responsible for introducting many new APIs and technologies such as the Sharepoint API, Microsoft ADAL.js and Microsoft Graph API to the organization.</p>",
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
    },
    {
      title: "CONSULTANT",
      company: "Capgemini",
      from: "February 2012",
      to: "August 2014",
      description: [
        "<p>Worked as a consultant in the projects listed below.</p>"
      ]
    },
    {
      title: "JAVA DEVELOPER",
      company: "VPC / Euroclear",
      from: "February 2012",
      to: "August 2014",
      description: [
        '<p>I joined this project as a fresh graduate and within a year advanced to main developer of the Java-based applications. I was also assigned to the "core" team consisting of 7 consultants out of the 25 employee strong team.</p>',
        "<ul><li>Estimation, analysis, debugging, documentation for incidents and change requests.</li><li>Held various project management duties; time-plans, team briefings and client meetings</li><li>Co-responsible for review of new hires, including training and code reviews.</li></ul>"
      ],
      words: [
        "Apache ANT",
        "Apache Commons",
        "Apache POI",
        "Apache Tomcat",
        "CSS",
        "CVS",
        "DB2 SQL",
        "Efecte",
        "HTML",
        "IBM Message Broker",
        "IBM Tivoli Access Manager",
        "WebSEAL",
        "iText",
        "Java",
        "Java EE",
        "Java Server Faces",
        "JavaMail",
        "JavaScript",
        "JIRA",
        "JMS",
        "LDAP",
        "MyFaces",
        "Spring",
        "WebSphere Application Server"
      ]
    },
    {
      title: "PROJECT MANAGER",
      company: "Capgemini",
      from: "December 2012",
      to: "August 2014",
      description: [
        "<p>Planning, executing and reviewing a successful and highly appreciated customer event consisting of three camps throughout each year for clients and fellow employees.</p><p>Responsibility for annual budget of SEK 150 000 with an audience of CxO level participants.</p>"
      ]
    },
    {
      title: "MASTER'S THESIS",
      company: "Configura",
      from: "August 2011",
      to: "December 2011",
      description: [
        "<p>I wrote my Master’s Thesis for the Linköping-based software company Configura. Configura develops 3D software used for space-planning and layouts in rooms and industrial environments. I quickly learned the various advantages and problem areas of the software and development processes. The finished thesis contained both an analysis of the current situation as well as suggestions for future improvements.</p>"
      ]
    }
  ];

  const educations = [
    {
      title: "M.Sc. Industrial Engineering and Management (Intl, Japanese)",
      school: "The Institute of Technology at Linköping University",
      from: "2006",
      to: "2011",
      description: [
        "<ul><li>Computer Science, which entails courses in programming (Java, Python, SQL and more), computer architecture as well as larger project-based advanced software engineering courses.</li><li>Industrial Marketing, focusing on the marketing function, and strategic management and positioning.</li></ul>"
      ]
    },
    {
      title: "Exchange Studies",
      school: "明治大学 / Meiji University, Tokyo",
      from: "2008",
      to: "2009",
      description: [
        "<p>Exchange student programme as part of the masters degree. All courses were given in Japanese, and consisted of business and management courses.</p>"
      ]
    },
    {
      title: "Foundation year in Japanology",
      school: "The Institute of Technology at Linköping University",
      from: "2005",
      to: "2006",
      description: [
        "<p>Preparation for International Programme - Japanese language studies, and to a lesser extent courses on Japanese culture and society.</p>"
      ]
    },
    {
      title: "High School - Natural Science Programme",
      school: "Stångådalens Gymnasium, Vimmerby",
      from: "2000",
      to: "2003",
      description: [""]
    }
  ];
</script>

<style type="text/scss">
  .cv {
    @media screen {
      max-width: 1200px;
      margin: 0px auto;
      background-color: #e6e6e8;
      background-size: contain;
      box-shadow: 0 19px 38px rgba(0, 0, 0, 0.3),
        0 15px 12px rgba(0, 0, 0, 0.22);
    }

    // background: url("static/ivory-paper.jpg");
    position: relative;
    z-index: 0;

    .name {
      min-width: 100%;
      background-color: #4d4d4f;
      color: #e6e6e8;
      z-index: 1;
      padding: 50px auto;

      img {
        border-radius: 50%;
        display: block;
        margin: 0 auto;
        width: 200px;
        margin: 25px auto;
      }

      p {
        text-align: center;
        margin: 25px 50px;
      }

      h1 {
        text-align: center;
      }
    }

    main {
      border-radius: 2px;
      z-index: 2;
      padding: 0 25px;
    }

    h2 {
      text-align: right;
    }

    .bottom-thing {
      margin: 20px auto;
    }

    @media screen and (min-width: 500px) {
      display: flex;
      flex-wrap: wrap;

      main {
        width: 65%;
      }

      .name {
        width: 100%;
        color: #e6e6e8;
        z-index: 3;

        div.img {
          width: 25%;
          float: left;
        }

        div.rest {
          width: 75%;
          float: left;
        }

        h1 {
          font-size: 5rem;
          margin: 0;
          text-align: center;
        }

        p {
          text-align: left;
          &:nth-of-type(2) {
            text-align: right;
          }
        }

        h2 {
          margin-top: 90px;
        }
      }
    }

    @media print {
      img {
        border-radius: 50%;
        display: none !important;
        margin: 0 auto;
        margin: 25px auto;
      }

      p {
        text-align: left;
        &:nth-of-type(2) {
          text-align: left;
        }
      }

      h2 {
        text-align: left;
      }

      .name p {
        display: none;
      }

      .bottom-thing {
        display: none;
      }
    }
  }
</style>

<div class="cv">

  <div class="name">

    <div class="img">
      <img {src} alt="Jonas" />
    </div>
    <div class="rest">

      <p>Hi, my name is</p>
      <h1 style="color: black;">Jonas Eriksson</h1>
      <h2 style="text-align: center;" />
      <p>
        ... and I am a
        <strong>FULLSTACK WEB DEVELOPER</strong>
      </p>
    </div>
  </div>

  <Sidebar />
  <main>
    <h2>EXPERIENCE</h2>
    {#each experiences as exp}
      <Experience
        title={exp.title}
        company={exp.company}
        from={exp.from}
        to={exp.to}
        description={exp.description}
        words={exp.words} />
    {/each}

    <h2>EDUCATION</h2>
    {#each educations as edu}
      <Education
        title={edu.title}
        from={edu.from}
        school={edu.school}
        to={edu.to}
        description={edu.description} />
    {/each}
  </main>

  <div class="bottom-thing">
    <hr />
    This site is built with
    <a href="https://www.svelte.dev">Svelte</a>
    &ndash; because I think it's pretty cool.
  </div>
</div>
