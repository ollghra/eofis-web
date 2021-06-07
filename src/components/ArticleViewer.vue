<template>
<div>
    <section class="section" v-for="article in FileThing" :key="article.id">
        <h1 class="title">{{article.Title}}</h1>
        <h2 class="subtitle">Flashcards automatically generated from <a :href="article.URL" target="_blank">this article.</a></h2>
<div class="columns is-multiline">
            <div v-for="card in article.Cards" :key="card.id" class="card box column is-one-quarter">
                <header class="card-header">
                    <p class="card-header-title">
                        {{card.Question}}
                    </p>
                </header>
                <div class="card-content">
                    <div class="content">
                        {{card.Answer}}
                    </div>
                </div>
            </div>
</div>
    </section>
</div>
<div class="icon-text">
  <span class="icon has-text-info">
    <i class="fas fa-info-circle"></i>
  </span>
  <span>Information</span>
</div>
</template>

<script>
import FileThing from '../../public/p1_out-tr_cq.json';
export default {
  name: 'Articles',
  props: {
    filepath: String
  },
    data() {
        return { FileThing }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
