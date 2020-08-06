<script>
  import Sidebar from "./Sidebar.svelte";
  import Experience from "./Experience.svelte";
  import Education from "./Education.svelte";

  const src = "static/jonas-bw-size.png";

  const experiences = [
    {
      title: "FULLSTACK DEVELOPER",
      company: "Reason Studios",
      from: "October 2017",
      to: "present",
      description: [
        "<ul><li>Quickly got up to speed in new languages for the position - Python & Django</li><li>Deeply involved in infrastructure and devops including build systems and servers/AWS</li><li>Technical responsibility for the web shop, which generates 75% of the companies revenue</li><li>Technical responsibility for authentication and the license system of the companies main products</li><li>True full stack development all the way from databases, APIs, microservices and frontend</li><li>Serving thousands of daily end users with always available systems</li></ul>"
      ],
      words: [
        "Ansible",
        "AWS",
        "CSS3",
        "Django",
        "Docker",
        "Electron",
        "Git",
        "HTML5",
        "Java",
        "JavaScript",
        "Jenkins",
        "Jinja2",
        "JIRA",
        "Linux",
        "MySQL",
        "postgres",
        "Python",
        "React",
        "REST",
        "SQL",
        "Vagrant"
      ]
    },
    {
      title: "FULLSTACK DEVELOPER (consultant)",
      company: "Swedish Police (via HiQ)",
      from: "June 2016",
      to: "October 2017",
      description: [
        "<ul><li>Primary frontend developer in project porting COBOL to modern web-based applications.</li><li>Also involved in significant Java backend development.</li><li>Delivered two of these applications far ahead of schedule</li><li>Introduced frontend build systems and testing to the team.</li></ul>"
      ],
      words: [
        "AngularJS",
        "CSS3",
        "Git",
        "HTML5",
        "Jasmine",
        "Java",
        "JavaScript",
        "LESS",
        "Maven",
        "REST"
      ]
    },
    {
      title: "FRONTEND DEVELOPER (consultant)",
      company: "Midroc (via HiQ)",
      from: "October 2014",
      to: "June 2016",
      description: [
        "<ul><li>Lead frontend developer in multiple projects, with big impact on UX and design decisions</li><li>Introduced many new technologies including AngularJS, Sharepoint APIs and Microsoft Graph</li><li>Developed new intranet - starting point for 1100 employees and 70 000+ views per month</li><li>Various other projects, including portals for project planning and time reporting</li></ul>"
      ],
      words: [
        "AngularJS",
        "Azure",
        "CSS3",
        "Git",
        "HTML5",
        "Jasmine",
        "JavaScript",
        "Microsoft Graph API",
        "Node",
        "npm",
        "OAuth2",
        "REST",
        "SCRUM",
        "Sharepoint Online",
        "TFS",
        "Yammer"
      ]
    },
    {
      title: "JAVA DEVELOPER (consultant)",
      company: "Euroclear (via Capgemini)",
      from: "February 2012",
      to: "August 2014",
      description: [
        "<ul><li>Advanced from graduate to lead developer of the projects Java services within the first year</li><li>Chosen to the 7 strong <em>core team</em> out of 25 total</li><li>Responsible for estimation, analysis, bugfixing and documentation of invidents and change requests</li><li>Project leader responsibilites for time plans, team briefings and client meetings</li><li>Shared responisibility for new hires, including interviews, training and core reviews</li></ul>"
      ],
      words: [
        "Apache Tomcat",
        "CSS",
        "CVS",
        "DB2",
        "HTML",
        "Java/Java EE",
        "JavaScript",
        "JIRA",
        "Spring"
      ]
    }
  ];

  const educations = [
    {
      title:
        "M.Sc. Industrial Engineering and Management (Inernational, Japanese)",
      school: "The Institute of Technology at Linköping University",
      from: "2005",
      to: "2011",
      description: [
        "<ul><li>Computer science - programming, computer architecture, larger project based software engineering courses.</li><li>Industrial Marketing - project management, strategic mangagement and positioning.</li><li>Preceeded by one year of Japanese courses</li></ul>"
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
      text-align: left;
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
      <h1>Jonas Eriksson</h1>
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
