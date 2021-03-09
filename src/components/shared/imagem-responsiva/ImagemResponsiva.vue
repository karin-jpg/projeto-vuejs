<template>
    <img class="imagem-responsiva" :src= "url" :alt = "titulo">
</template>

<script>
export default {
    //props: ['url', 'titulo']
    props: {
      url: {
        type: Array,
        required: true
      },
      titulo: {
        type: Array,
        required: true
      }
    }
}
</script>

<style scoped>

 .imagem-responsiva {
    width: 100%;
  }

</style>