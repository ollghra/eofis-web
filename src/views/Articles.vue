<template>
  <div class="articles">
    <ArticleViewer filepath="p1-tr_cq.json"/>
  </div>
</template>

<script>
// @ is an alias to /src
import ArticleViewer from '@/components/ArticleViewer.vue'

export default {
  name: 'Articles',
  components: {
    ArticleViewer
  }
}
</script>
