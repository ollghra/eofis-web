<template >
    <div class="column is-one-quarter card" v-if="visible">
        <div class="card-content">
            <p class="has-text-primary-dark">
            {{question}}
            </p>
    <p class="has-text-white-bis has-background-dark">
    <strong>{{answer}}</strong>
    </p>
        </div>
        <footer class="card-footer">
            <span class="card-footer-item icon-text has-text-success">
                <span class="icon is-medium">
                    <i class="fas fa-check"></i>
                </span>
            </span>
            <span class="card-footer-item icon-text has-text-danger"
                      @click="hide">
                <span class="icon is-medium has-text-danger">
                    <i class="fas fa-trash-alt"></i>
                </span>
            </span>
            <span class="card-footer-item icon-text has-text-info">
                <span class="icon is-medium has-text-info">
                    <i class="fas fa-ellipsis-v"></i>
                </span>
            </span>
        </footer>
    </div>
</template>
<script>
    export default {
            name: 'Card',
            props: {
                    question: String,
                    answer: String
                },
            data() {
                    return {
                            visible : true
                        }
                },
            methods: {
                    hide() {
                            this.visible = false;
                        }
                }
        }
</script>
<style scoped>
.column {
    margin: 0.5rem;
}
.card-content {
    flex: auto;
    height: 80%;
}
.card-footer {
    margin-top: auto;
}
.icon, .icon-text {
    pointer-events: initial;
}
.icon-text:hover {
    font-weight: bold;
    background: #0f0f0f;
    color: white;
}

</style>
