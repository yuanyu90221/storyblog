<template>
  <div id="posts">
    <PostPreview
      v-for="post in posts"
      :id="post.id"
      :key="post.id"
      :title="post.title"
      :thumbnail-image="post.thumbnailUrl"
      :excerpt="post.previewText"
    />
  </div>
</template>

<script>
import PostPreview from '@/components/Blog/PostPreview'
export default {
  components: {
    PostPreview
  },
  data () {
    return {
      posts: [
        {
          title: 'A New Beginning',
          previewText: 'This will be awesome, don\'t miss it',
          thumbnailUrl: 'https://i.imgur.com/9f6538R.png',
          id: 'a-new-beginning'
        },
        {
          title: 'A Second Beginning',
          previewText: 'This will be awesome, don\'t miss it',
          thumbnailUrl: 'https://i.imgur.com/9f6538R.png',
          id: 'a-second-beginning'
        }
      ]
    }
  }
}
</script>

<style>
#posts {
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>
