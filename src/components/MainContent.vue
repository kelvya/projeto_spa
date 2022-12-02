<template>
    <p class="mt-3">{{ info }}</p>
    <hr />
    <ul class="list-inline">
        <li v-for="p in pratos" :key="p.id">{{ p.opcao }}</li>
    </ul>
    <button @click="showHideContato" class="btn btn-info">Clique para contato</button>
    <p v-show="showContato" class="mt-2">ristorant1339@gmail.com</p>
    <p v-show="showContato" class="mt-2"><a href="tel:11 999990000"> tel:11 999990000</a></p>
    <div v-show="showContato">
        <FormContato/>
    </div>
</template>

<script>
import FormContato from './forms/FormContato.vue'
export default {
  name: 'MainContent',
  data(){
    return{
        info: 'Conheça nossos pratos',
        showContato: false,
        pratos: [
            {id:1, opcao: 'Salmão Grelhado'}, 
            {id:2, opcao: 'Feijoada Light'}, 
            {id:3, opcao: 'Penne ao Sugo'}
        ]
    }
  },
    methods: {
        showHideContato() {
            this.showContato = !this.showContato
            console.log(this.showContato)
        }
    },
    components:{
        FormContato
    }
}
</script>

<style scoped>
li::before{
    content:'+';
}
</style>