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
  <a href="/projects" slot="header-main">Projects</a>
  <a href="/contact" slot="header-right">Contact</a>
</Header>

<main>
  <h1>Projects</h1>
</main>

<style>
</style>