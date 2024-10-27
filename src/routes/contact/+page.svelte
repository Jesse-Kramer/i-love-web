<script>
  // Components
  import Header from '../../components/header.svelte';
  import MessageApp from '../../components/message-app.svelte';

  const messages = [
    { type: 'incoming', text: 'Hi, someone wants your contact info. Can you send me your e-mail real quick?' },
    { type: 'outgoing', text: 'Yeah sure, I\'m available for work from the 1st of November. My e-mail is <a href="mailto:jesse-kramer@hva.nl">jesse.kramer@hva.nl</a>' },
    { type: 'status', text: 'Read' }
  ];

  // View-transitions
  import ViewTransition  from '../../lib/ViewTransition.svelte';
</script>

<ViewTransition>
  <Header>
    <a href="./" slot="header-left">About me</a>
    <a href="/contact" slot="header-main">Contact</a>
    <a href="/playground" slot="header-right">Playground</a>
  </Header>
  
  <main>
    <section class="page-intro">
      <p>Let's</p>
      <p>Work</p>
      <p>Together</p>
    </section>
  
    <MessageApp {messages} />
  </main>
</ViewTransition>


<style>
  section.page-intro p:nth-of-type(3) {
    text-decoration: underline;
  }

</style>