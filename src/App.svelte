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
      description: `<ul>
        <li>Heavily involved in infrastructure and devops including build systems and servers/AWS</li>
        <li>Serving 10 000+ daily end users with always available systems</li>
        <li>Technical responsibility for the web shop, generating 75% of company revenue</li>
        <li>Technical responsibility for authentication and the license systems</li>
        <li>True full stack development from databases via APIs and microservices to frontend</li>
        <li>Quickly got up to speed in new frameworks - Python & Django</li>
        </ul>`
    },
    {
      title: "FULLSTACK DEVELOPER (consultant)",
      company: "Polisen (via HiQ)",
      from: "June 2016",
      to: "October 2017",
      description: `<ul>
          <li>Lead frontend developer porting COBOL systems to modern web-based applications</li>
          <li>Also included significant Java backend development</li>
          <li>Deliverables finished far ahead of schedule</li>
          <li>Introduced the team to frontend build systems and testing</li>
        </ul>`
    },
    {
      title: "FRONTEND DEVELOPER (consultant)",
      company: "Midroc (via HiQ)",
      from: "October 2014",
      to: "June 2016",
      description: `<ul>
          <li>Lead frontend developer in multiple projects</li>
          <li>Large influence on UX and design decisions</li>
          <li>Introduced new technologies incl. AngularJS, Sharepoint APIs and Microsoft Graph</li>
          <li>Developed new intranet - start page for 1100 employees and 70 000+ views/month</li>
          <li>Various other projects, including portals for project planning and time reporting</li>
        </ul>`
    },
    // {
    //   title: "-- IT CONSULTANT --",
    //   company: "Capgemini",
    //   from: "February 2012",
    //   to: "August 2014",
    //   description: "<p>Worked as a consultant with the project listed below</p>"
    // },
    {
      title: "JAVA DEVELOPER (consultant)",
      company: "Euroclear (via Capgemini)",
      from: "February 2012",
      to: "August 2014",
      description: `<ul>
          <li>Advanced from graduate to lead developer of the Java services within the first year</li>
          <li>Chosen to the 7 employee <em>core team</em> out of total 25 employees</li>
          <li>Responsible for estimation, analysis, bugfixing and documentation of incidents and change requests</li>
          <li>Project leader responsibilites for time plans, team briefings and client meetings</li>
          <li>Shared responisibility for new hires, including interviews, training and core reviews</li>
        </ul>`
    }
  ];

  const educations = [
    {
      title:
        "M.Sc. Industrial Engineering and Management (International, Japanese)",
      school: "The Institute of Technology at Linköping University",
      from: "2005",
      to: "2011",
      description: `<ul>
          <li>Computer science - programming, computer architecture, larger project based software engineering courses.</li>
          <li>Industrial Marketing - project management, strategic mangagement and positioning.</li>
          <li>Preceeded by one year of Japanese courses</li>
        </ul>`
    },
    {
      title: "Exchange Studies",
      school: "明治大学 / Meiji University, Tokyo",
      from: "2008",
      to: "2009",
      description: `
        <p>Exchange student programme as part of the masters degree. All courses were given in Japanese, and consisted of business and management courses.</p>
      `
    }
  ];
</script>

<style lang="scss">
  @page {
    size: auto;
    margin: 0;
  }

  body {
    /* this affects the margin on the content before sending to printer */
    margin: 0px;
  }

  .cv {
    max-width: 1200px;
    margin: 0px auto;
    background-color: #e6e6e8;
    background-size: contain;
    @media screen {
      box-shadow: 0 19px 38px rgba(0, 0, 0, 0.3),
        0 15px 12px rgba(0, 0, 0, 0.22);
      background: url("static/ivory-paper.jpg");
    }
    position: relative;
    z-index: 0;
    padding-bottom: 50px;

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
        margin: 25px 25px;
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
    @media print {
      h1 {
        size: 50%;
      }
      .screen-only {
        display: none;
      }
      .name {
        color: black;
        border-bottom: 1px solid gray;
      }

      img {
        max-width: 100px;
      }

      .rest {
        display: flex;
        height: 100%;
        align-items: center;
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
      <p class="screen-only">Hi, my name is</p>
      <h1>Jonas Eriksson</h1>
      <p class="screen-only">
        ... and I am a
        <strong>FULLSTACK WEB DEVELOPER</strong>
      </p>
    </div>
  </div>

  <Sidebar />
  <main>
    <h2>EXPERIENCE</h2>
    {#each experiences as exp}
      <Experience {...exp} />
    {/each}

    <h2 style="margin-top: 20px;">EDUCATION</h2>
    {#each educations as edu}
      <Education
        title={edu.title}
        from={edu.from}
        school={edu.school}
        to={edu.to}
        description={edu.description} />
    {/each}
  </main>

  <div class="bottom-thing screen-only">
    <hr />
    This site is built with
    <a href="https://www.svelte.dev">Svelte</a>
    &ndash; because I think it's pretty cool.
  </div>
</div>
