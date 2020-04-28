<script>
  import data from '../instagram.json';
  const photos = data.graphql.hashtag.edge_hashtag_to_media.edges;

  function truncate_words(text, length) {
    if (text.length <= length) {
      return text;
    } else {
      return `${text.slice(0, length)}...`;
    }
  }
</script>

<div class="container photolist">
  {#each photos as photo}
    <div class="card">
      <figure class="image">
        <img src="{photo.node.thumbnail_src}" alt="thumbnail" />
      </figure>
      <div class="card-content">
        <div class="content">
          <p>{truncate_words(photo.node.edge_media_to_caption.edges[0].node.text, 200)}</p>
        </div>
      </div>
    </div>
  {/each}
</div>
<style>
  .container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
    grid-gap: 0.5em;
  }

  .card {
    max-width: 90%;
    height: max-content;
    border: 1px solid #cacaca;
    box-shadow: 5px 5px 5px 0px rgba(202, 202, 202, 1);
  }
</style>
