<template>
    <button @click= "disparaAcao()" class="botao" :class= "estiloDoBotao" :type = "tipo">{{ rotulo }}</button>
</template>

<script>
export default{

    props: {
        tipo: {
            type: Array,
            required: true
        },
        rotulo: {
            type: Array,
            required: true
        },
        confirmacao: {
            type: Boolean,
            required: false
        },
        estilo: {
            type: String,
            required: false
        }
    },
    methods: {
        disparaAcao(){
            if(this.confirmacao){
               if(confirm("Confirma operação?")){
                    this.$emit('botaoAtivado');
                }
            }else{
                this.$emit('botaoAtivado');
            }
            
        }
    },

    computed: {
        estiloDoBotao(){
            if(this.estilo == "padrao" || !this.estilo) return 'botao-padrao';
            if(this.estilo == "perigo") return 'botao-perigo'
        }
    }

}

</script>

<style scoped>
    .botao {
        display: inline-block;
        padding: 10px;
        border-radius: 3px;
        margin: 10px;
        font-size: 1.2em;
    }

    .botao-perigo {
        background: firebrick;
        color: white;
    }

    .botao-padrao {
        background: darkcyan;
        color: white;
    }
</style>