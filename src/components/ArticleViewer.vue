<template>
    <div>
        <section class="section" v-for="article in FileThing" :key="article.id">
            <h1 class="title">{{article.Title}}</h1>
            <h2 class="subtitle">Flashcards automatically generated from <a :href="article.URL" target="_blank">this article.</a></h2>
            <div class="columns is-multiline">
                <div v-for="card in article.Cards" :key="card.id" class="box column is-one-quarter">
                    <p class="has-text-primary-dark">
                        {{card.Question}}
                    </p>
                    <p class="has-text-white-bis has-background-dark">
                        <strong>{{card.Answer}}</strong>
                    </p>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import FileThing from '../../public/p1_out-vht5_b.json'
//import FileThing from '../../public/p1_out-tr_cq.json';
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
