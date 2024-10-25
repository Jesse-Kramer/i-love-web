<script>
  import Header from '../../components/header.svelte';
  import { onNavigate } from '$app/navigation';

    onNavigate((navigation) => {
        if (!document.startViewTransition) return;

        return new Promise((resolve) => {
            document.startViewTransition(async () => {
                resolve();
                await navigation.complete;
            });
        });
    });
</script>

<Header>
  <a href="./" slot="header-left">About me</a>
  <a href="/playground" slot="header-main">Playground</a>
  <a href="/contact" slot="header-right">Contact</a>
</Header>

<main>
  <section class="stuff">
    <article>
      <h2>Notes</h2>
      <ul>
        <li>
          <h3>I Love Web</h3>
          <a href="https://github.com/Jesse-Kramer/i-love-web/wiki/We-%E2%9D%A4%EF%B8%8F-web#vasilis-van-gemert---13-09-2024" target="_blank">Vasilis van Gemert - 13-09-2024</a>
        </li>
  
        <li>
          <h3>I Love Web</h3>
          <a href="https://github.com/Jesse-Kramer/i-love-web/wiki/We-%E2%9D%A4%EF%B8%8F-web#dion-pieters---18-10-2024" target="_blank">Dion Pieters - 18-10-2024</a>
        </li>
      </ul>
    </article>
    <article>
      <h2>Projects</h2>
      <ul>
        <li>
          <h3>Personal project</h3>
          <a href="https://jesse-kramer.nl/" target="_blank">Profile card & portfolio - N/A</a>
        </li>
        <li>
          <h3>School project</h3>
          <a href="https://github.com/christoph3r3w/pleasurable-ui" target="_blank">Redpers - Sprint 11</a>
        </li>
        <li>
          <h3>School project</h3>
          <a href="https://github.com/Jesse-Kramer/tumi-mundo" target="_blank">Tumi Mundo - Actively working on</a>
        </li>
      </ul>
    </article>
    <article>
      <h2>Other</h2>
      <ul>
        <li>
          <h3>N/A</h3>
          <a href="/">N/A</a>
        </li>
      </ul>
    </article>
  </section>
  <section class="progress">
    <p>More soon</p>
  </section>

</main>

<style>
  .stuff {
    display: flex;
    width: 100%;
    flex-wrap: wrap;
    align-content: center;
    align-items: flex-start;
    justify-content: space-evenly;
  }
  section.stuff h2 {
    margin-bottom: .5em;
  }

  section article li {
    margin-bottom: 1em;
  }

  section article h3, section article a {
    font-size: 1.5em;
  }

  section.progress {
    margin-top: 15em;
    text-align: center;
  }

  section.progress p {
    font-size: 5em;
  }

  @media screen and (max-width: 800px) {
      section.stuff h2 { 
        font-size: 2.5em;
      }

      section article h3, section article a {
        font-size: 1em;
      }
  }

  @media screen and (max-width: 500px) {
    .stuff {
      flex-direction: column;
      align-content: space-around;
    }
  }
</style>