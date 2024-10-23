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
  <a href="/projects" slot="header-right">Projects</a>
</Header>

<main>
  <h1>Contact</h1>
</main>

<style>
</style>