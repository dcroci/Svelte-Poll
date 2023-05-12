<script>
  //imports
  import Header from './components/header.svelte';
  import Footer from './components/footer.svelte';
  import Tabs from './components/shared/Tabs.svelte';
  import CreatePollForm from './components/CreatePollForm.svelte';
  //variables
  let items = ['Current Polls', 'Create New Poll'];
  let activeItem = 'Current Polls';
  //functions
  const tabChange = (e) => {
    activeItem = e.detail;
  };
</script>

<Header />
<main>
  <Tabs {activeItem} {items} on:tabchange={tabChange} />
  {#if activeItem === 'Current Polls'}
    <p>Poll List Component Here</p>
  {:else}
    <CreatePollForm />
  {/if}
</main>
<Footer />

<style>
  main {
    max-width: 960px;
    margin: 40px auto;
  }
</style>
