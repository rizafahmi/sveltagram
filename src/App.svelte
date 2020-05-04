<script>
  import BigHeader from './components/BigHeader.svelte';
  import PhotoList from './components/PhotoList.svelte';
  import Ribbon from './components/Ribbon.svelte';

  export let hashtag;
</script>

<svelte:head>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/bulma/0.8.0/css/bulma.min.css" rel="stylesheet" />
</svelte:head>

<Ribbon />
<main class="container">
  <BigHeader hashtag={hashtag} />
  <PhotoList />
</main>

<style>
</style>
