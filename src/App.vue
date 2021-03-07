<template>
<div>
<h1>{{titulo}}</h1>
<ul>
  <li v-for= "foto of fotos" :key= "foto.id">
    <img :src = " foto.url " :alt = "foto.titulo">
    </li>
</ul>


</div>
</template>

<script>
export default {

  data(){

    return{
      titulo: 'GatoPic',
      fotos: [
        {
          id: 1,                                                                                                               
          url: 'https://www.proteste.org.br/-/media/proteste/images/home/alimentacao/seguranca-alimentar/gato-nao-come.jpg?rev=b16a475f-961e-45ab-8f5d-12550b00b87c',
          titulo: 'gato'
        },
        {
          id: 2,
          url: 'https://www.petz.com.br/blog/wp-content/uploads/2019/07/vida-de-gato.jpg',
          titulo: 'gatin'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
</style>
