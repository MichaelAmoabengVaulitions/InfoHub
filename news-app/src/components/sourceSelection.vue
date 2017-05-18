<template>
    <div class="sourceselection">
        <h4>Select News Source</h4>
        <select class="form-control" v-on:change="sourceChanged">
            <option v-bind:value="source.id" v-for="source in sources">{{ source.name }}</option>
        </select>
    </div>

</template>

<script>
    export default {
        name: 'sourceSelection',
        data () {
            return {
            sources: [],
            source: ''
            }
        }
    }
</script>

<style scoped>

</style>