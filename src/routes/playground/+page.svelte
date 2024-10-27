<script>
  import Header from '../../components/header.svelte';
  // View-transitions
  import ViewTransition  from '../../lib/ViewTransition.svelte';

  const resources = [
    {
      category: "Notes",
      items: [
        {
          title: "I Love Web",
          link: "https://github.com/Jesse-Kramer/i-love-web/wiki/We-%E2%9D%A4%EF%B8%8F-web#vasilis-van-gemert---13-09-2024",
          description: "Vasilis van Gemert - 13-09-2024",
        },
        {
          title: "I Love Web",
          link: "https://github.com/Jesse-Kramer/i-love-web/wiki/We-%E2%9D%A4%EF%B8%8F-web#dion-pieters---18-10-2024",
          description: "Dion Pieters - 18-10-2024",
        },
      ],
    },
    {
      category: "Projects",
      items: [
        {
          title: "Personal project",
          link: "https://jesse-kramer.nl/",
          description: "Profile card & portfolio - N/A",
        },
        {
          title: "School project",
          link: "https://github.com/christoph3r3w/pleasurable-ui",
          description: "Redpers - Sprint 11",
        },
        {
          title: "School project",
          link: "https://github.com/Jesse-Kramer/tumi-mundo",
          description: "Tumi Mundo - Actively working on",
        },
      ],
    },
    {
      category: "Other",
      items: [
        {
          title: "N/A",
          link: "/",
          description: "N/A",
        },
      ],
    },
  ];

</script>

<ViewTransition>
  <Header>
    <a href="./" slot="header-left">About me</a>
    <a href="/playground" slot="header-main">Playground</a>
    <a href="/contact" slot="header-right">Contact</a>
  </Header>
  
  <main>
    <section class="resources-section">
      {#each resources as resource}
        <article>
          <h2>{resource.category}</h2>
          <ul>
            {#each resource.items as item}
              <li>
                <h3>{item.title}</h3>
                <a href={item.link} target="_blank">{item.description}</a>
              </li>
            {/each}
          </ul>
        </article>
      {/each}
    </section>  
    <section class="progress-section">
      <p>More soon</p>
    </section>
  
  </main>
</ViewTransition>

<style>
  .resources-section {
    display: flex;
    width: 100%;
    flex-wrap: wrap;
    align-content: center;
    align-items: flex-start;
    justify-content: space-evenly;
  }
  section.resources-section h2 {
    margin-bottom: .5em;
  }

  section article li {
    margin-bottom: 1em;
  }

  section article h3, section article a {
    font-size: 1.5em;
  }

  section.progress-section {
    margin-top: 15em;
    text-align: center;
  }

  section.progress-section p {
    font-size: 5em;
  }

  @media screen and (max-width: 800px) {
      section.resources-section h2 { 
        font-size: 2.5em;
      }

      section article h3, section article a {
        font-size: 1em;
      }
  }

  @media screen and (max-width: 500px) {
    .resources-section {
      flex-direction: column;
      align-content: space-around;
    }
  }
</style>