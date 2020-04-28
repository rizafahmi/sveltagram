<script>
  import BigHeader from './components/BigHeader.svelte';
  export let hashtag;
</script>

<main>
  <BigHeader hashtag={hashtag} />
  <input type="text" bind:value={hashtag} />
</main>

<style>
</style>
