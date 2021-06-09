<style scoped>
li.expandable-list ul {
    display: none;
}
li.expandable-list.expanded ul {
    display: block;
}
li.expandable-list.expanded a.arrow {
    background: url(../assets/arrow-open.gif) no-repeat;
}
li.expandable-list a.arrow {
    width: 8px;
    height: 8px;
    display: inline-block;
    background: url(../assets/arrow-close.gif) no-repeat;
    border-bottom: 0;
    padding-right: 4px;
}

ul.tutorial-index {
    margin: 0;
    padding-left: 0;
}
ul.tutorial-index > li:before {
    display: none;
}

aside {
    float: left;
    margin-left: 32px;
    /*    width: 200px;*/
}
aside ul {
    padding: 0;
    list-style: none;
    margin: 0;
}
aside ul li {
    padding: 0;
    margin: 0 0 0 1em;
    text-indent: -1em;
}
</style>
<template>
<!--    <aside>
        <h1>My Library</h1>
        <ul class="library-index">
            <li class="expandable-list" :class="{expanded: isExpanded}"><a href="javascript:void(0)" class="arrow" v-on:click="toggleExpand"></a><a href="javascript:void(0)">First category</a>
                <ul class="library-index">
                    <li><a href="javascript:void(0)">First subdeck</a></li>
                    <li><a href="javascript:void(0)">Second subdeck</a></li>
                    <li><a href="javascript:void(0)">Third subdeck</a></li>
                </ul>
            </li>
            <li class="expandable-list"><a href="javascript:void(0)" class="arrow"></a><a href="javascript:void(0)">Second category</a>
                <ul class="library-index">
                    <li><a href="javascript:void(0)">2. First subdeck</a></li>
                    <li><a href="javascript:void(0)">2. Second subdeck</a></li>
                </ul>
            </li>
        </ul>
    </aside>
-->
    <div class="container">
        <Article v-for="article in JSON_Politics" :key="article.id"
                 :article="article"/>
    </div>
</template>

<script>
    import JSON_Politics from '../../public/p1_out-vht5_b.json'
    //import JSON_Politics from '../../public/p1_out-tr_cq.json';
    import Article from './Article.vue';
    export default {
            name: 'ArticleViewer',
            props: {
                    filepath: String,
                },
            data() {
                    return { 
                            JSON_Politics,  
                            isExpanded: false
                        }
                },
            methods: {
                    toggleExpand() {
                            this.isExpanded = !this.isExpanded;
                        }
                },
            components: {
                    Article
                }
        }
</script>

