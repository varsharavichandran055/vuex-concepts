<template>
    <button @click="addOne">Add 2</button>
</template>

<script>
export default {
    methods:{
        addOne(){
            // this.$store.state.counter++;
            // this.$store.commit('increment');  //exmaple for mutation
            this.$store.dispatch('increment');  //exmaple for action

        }
    }
}
</script>