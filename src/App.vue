<template>
  <HeaderContent/>  
  <NavBar/>
  <SobreNos/>
  <MainContent/>  
  <FooterContent/>

  <div class="boxSetoresMain">
    <SetoresContato>
      <h3>Reservas</h3>
      <template #emailSetor="{ email }">
        Email: {{ email.email_reservas }}
      </template>
    </SetoresContato>
    
    <SetoresContato>
      <h3>Financeiro</h3>
      <template #emailSetor="{ email }">
        Email: {{ email.email_financeiro }}
      </template>
      <hr/>
      
    </SetoresContato>
    
    <SetoresContato>
      <h3>Outras informações</h3>
      <template #emailSetor>
      </template>
    </SetoresContato>
  </div>

  <TemplateRefs msg="Exemplo: Templete Refs"/>
  <hr/>
  <TemplateRefsVfor />
</template>

<script>
import HeaderContent from './components/HeaderContent'
import NavBar from './components/NavBar'
import SobreNos from './components/SobreNos'
import MainContent from './components/MainContent'
import FooterContent from './components/FooterContent'
import SetoresContato from './components/SetoresContato'
import TemplateRefs from './components/TemplateRefs.vue'
import TemplateRefsVfor from './components/TemplateRefsVfor.vue'


export default {
  name: 'App',
  components: {
    NavBar,
    HeaderContent,
    MainContent,
    FooterContent,
    SobreNos,
    SetoresContato,
    TemplateRefs,
    TemplateRefsVfor
},
  data(){
    return{
      //
    }
  },
}
</script>

<style>
a{
  color: red;
}

.boxSetoresMain{
  display: flex;
}
</style>