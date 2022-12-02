
<script>
import { h } from 'vue'
function sobreInfo(titulo, url, texto){
    const vnode = 
    h('div', {class: 'border p-2'}, [
        h('h3', {id:'tituloSobre', class: 'border p-2 bg-warning text-white px-3'}, titulo),
        h('div', {class:'d-flex'},[
            h(<img src={url} class="w-25" />),
            h(<p class="destaque px-4">{texto}</p>)
        ])
    ])
    return vnode
}

export default{
    data(){
        return{
            titulo: 'Sobre Nosso Ristorante',
            urlImage: require('@/assets/produtos/beef-g66eb2a540_1920.jpg'),
            texto: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae alias eum officiis eveniet, error itaque repellat harum veritatis quam? Animi? Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae alias eum officiis eveniet, error itaque repellat harum veritatis quam? Animi? Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae alias eum officiis eveniet, error itaque repellat harum veritatis quam? Animi? Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae alias eum officiis eveniet, error itaque repellat harum veritatis quam? Animi?'
        }
    },
    render(){
        return sobreInfo(this.titulo, this.urlImage, this.texto)
    }
}
</script>

