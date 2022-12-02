<template>
    <h1 ref="title">Bora codar com {{ vue }} Js!</h1>
</template>

<script>
    export default{
        name: 'MeuComp',
        data(){
            return{
                vue: 'Vue 4'
            }
        },
        // beforeCreate() {
        //     console.log('beforeCreate', 'Antes de criar a instância Vue')
        //     console.log('Data', this.vue)
        //     console.log('DOM', this.$refs.title)
        // },
        // created(){
        //     console.log('beforeCreate', 'Instância criada')
        //     console.log('Data', this.vue)
        //     console.log('DOM', this.$refs.title)
        // },
        // beforeMount() {
        //     console.log('beforeMount', 'Antes de montar o elemento')
        //     console.log('Data', this.vue)
        //     console.log('DOM', this.$refs.title)
        // },
        // mounted() {
        //     console.log('Mounted', 'Montagem concluída')
        //     console.log('Data', this.vue)
        //     console.log('DOM', this.$refs.title)
        // },
        // beforeUpdate() {
        //     console.log('beforeUpdate', 'Antes de atualizar os dados')
        //     console.log('Data', this.vue)
        //     console.log('DOM', this.$refs.title)
        // },
        // updated() {
        //     console.log('updated', 'Atualização concluída')
        //     console.log('Data', this.vue)
        //     console.log('DOM', this.$refs.title)
        // },
        beforeUnmount() {
            console.log('beforeUnmount', 'Antes de desmontar')
            console.log('Data', this.vue)
            console.log('DOM', this.$refs.title)
        },
        unmounted() {
            console.log('unmounted', 'Desmontagem concluída')
            console.log('Data', this.vue)
            console.log('DOM', this.$refs.title)
        }
    }

</script>