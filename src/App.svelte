<script>
  import BigHeader from './components/BigHeader.svelte';
  import PhotoList from './components/PhotoList.svelte';

  export let hashtag;
</script>

<main>
  <BigHeader hashtag={hashtag} />
  <div>
    <input type="text" bind:value={hashtag} />
  </div>
  <PhotoList />
</main>

<style>
</style>
