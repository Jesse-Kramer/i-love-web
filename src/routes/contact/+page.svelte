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
  <a href="/contact" slot="header-main">Contact</a>
  <a href="/playground" slot="header-right">Playground</a>
</Header>

<main>
  <section class="entry">
    <p>Let's</p>
    <p>Work</p>
    <p>Together</p>
  </section>
  <section class="message-app">
    <p class="incoming">Hi, someone wants your contact info. Can you send me your e-mail real quick?</p>
    <p class="outgoing">Yeah sure, I'm available for work from the 1st of november. My e-mail is <a href="mailto:jesse-kramer@hva.nl">jesse.kramer@hva.nl</a></p>
    <p class="status">Read</p>
  </section>

  <section class="mobile message-app">
    <p class="incoming">Bro, I thought they taught to build mobile first. 😂</p>
    <p class="outgoing">Uhm, yeah I did desktop first 💀, but I'm going to build the mobile version soon!📱</p>
    <p class="status">Read</p>
</section>
</main>

<style>
  section.entry p:nth-of-type(3) {
    text-decoration: underline;
  }  
</style>