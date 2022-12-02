<template>
    <h4 class="p-x4">Entre em contato enviando sua mensagem</h4>
    <form action="" @submit="confirmar($event)" class="border p-3 w-50">
        <InputText :id="idNome" name="nome" placeholder="Seu nome aqui"/>
        <InputText id="email" name="email" placeholder="Seu email aqui" />
        <TextArea/>
        <ButtonForm/>
    </form>
</template>

<script>
import InputText from './InputText.vue';
import TextArea from './TextArea.vue';
import ButtonForm from './ButtonForm.vue';
export default{
    name: 'FormContato',
    data(){
        return{
            idNome: 'Nome cliente'
        }
    },
    components: {
        InputText,
        TextArea,
        ButtonForm
    },
    methods:{
        confirmar(e){
            e.preventDefault()
            console.log(e.target.nome.value)
            console.log(e.target.email.value)
            console.log(e.target.comentarios.value)

        }
    }
}

</script>
