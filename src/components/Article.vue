<template>
    <div class="tile is-ancestor">
        <div>
            <h2>{{article.Title}}</h2>
            <h4>Source URL: <a :href="article.URL" target="_blank">this article.</a></h4>
            <button @click="Expand">Show Generated Flashcards</button>
        </div>
        <div v-if="expanded" class="article-container">
            <div class="columns is-multiline">
                <Card v-for="card in article.Cards" :key="card.id" 
                      :question="card.Question"
                      :answer="card.Answer"/>
            </div>
        </div>
    </div>
</template>
<script>
    import Card from './Card.vue';
    export default {
            name: 'Article',
            props: {
                    article: String
                },
            data() {
                    return { 
                            expanded: false
                        }
                },
            methods: {
                    Expand() {
                            this.expanded = !this.expanded;
                        }
                },
            components: {
                    Card
                }
        }
</script>
<style scoped>
h2 {
    font-weight: bold;
}
.columns {
    padding: 0.5rem;
    margin: 0;
}
.article-container {
    margin: 0px;
    padding: 1rem;
}
</style>
