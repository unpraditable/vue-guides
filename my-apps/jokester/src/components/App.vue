<template>
    <div id="app">
        <h3>Got Jokes?</h3>
        <button class="btn btn-primary" @click="initJokes">Add Ten Random Jokes</button>
        <br>
        <br>
            <Joke
                v-for="(joke, index) in $store.state.jokes" :joke="joke"
                key="index"
            />
    </div>
</template>

<script>
    import {mapActions} from 'vuex'
    import Joke from './Joke.vue'
    export default {
        methods: mapActions([
            'initJokes'
        ]),
        components: {
            Joke
        }
    }
</script>