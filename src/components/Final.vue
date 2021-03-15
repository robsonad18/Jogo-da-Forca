<template>
    <div class="final">
        <div class="final-texto">
            <span :class="`${etapa}`">{{texto}}</span>
        </div>

        <button 
            class="final-botao"
            v-on:click="jogarNovamente"    
        >Jogar novamente</button>
    </div>
</template>

<script>

export default{
    name: 'Final',
    props: {
        etapa: String,
        texto: String,
        jogarNovamente: Function
    },
    data() {
        return {
        }
    },
    methods: {
        
    },
    components: {
    }    
}
</script>

<style>
    .final-texto {
        margin: 20px 0px;
        font-size: 24px;
        font-weight: bold;
    }

    .ganhador {
        color: green;
    }

    .enforcado {
        color: red;
    }


</style>