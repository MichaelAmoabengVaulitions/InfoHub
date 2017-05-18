<template>
    <div class="sourceselection">
        <h4>Select News Source</h4>
        <select class="form-control" v-on:change="sourceChanged">
            <option v-bind:value="source.id" v-for="source in sources">{{source.name}}</option>
        </select>
    </div>

</template>

<script>
    export default {
        name: 'sourceselection',
        data () {
            return {
            sources: [],
            source: ''
            }
        },
        methods: {
            sourceChanged: function (e) {
                for(var i=0; i<sources.length; i++){
                    if(this.sources[i].id == e.target.value) {
                        this.source = this.sources[i];
                    }
                }
            }
        },
        created: function () {
            this.$http.get('https://newsapi.org/v1/sources?language=en')
                .then(response => {
                    this.sources = response.data.sources;
                })
        }
    }
</script>

<style scoped>

</style>