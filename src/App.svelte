<script>
  import Header from './components/header.svelte';
  import Footer from './components/footer.svelte';
  import Tabs from './components/shared/Tabs.svelte';
  let items = ['Current Polls', 'Create New Poll'];
  let activeItem = 'Current Polls';
  const tabChange = (e) => {
    activeItem = e.detail;
  };
</script>

<Header />
<main>
  <Tabs {activeItem} {items} on:tabchange={tabChange} />
</main>
<Footer />

<style>
  main {
    max-width: 960px;
    margin: 40px auto;
  }
</style>
