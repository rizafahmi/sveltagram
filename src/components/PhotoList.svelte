<script>
  import data from '../instagram.json';
  const photos = data.graphql.hashtag.edge_hashtag_to_media.edges;
</script>

<svelte:head>
  <link href="./PhotoList.css" rel="stylesheet" />
</svelte:head>
<div>
  <ul>
    {#each photos as photo}
      <li>
        <img src="{photo.node.thumbnail_src}" alt="thumbnail" />
        <p>{photo.node.edge_media_to_caption.edges[0].node.text}</p>
      </li>
    {/each}
  </ul>
</div>
<style></style>
