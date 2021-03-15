<template>
    <div class="teclado">
        <button class="teclado-botao" 
            v-for="(letra, key) in 'abcdefghijklmnopqrstuvxwyz'" 
            :key="key"
            :disable="verificarLetra(letra)"
            v-on:click="jogar(letra)"
            >
            {{letra}}
            </button>
    </div>
</template>

<script>

export default{
    name: 'Teclado',
    props: {
        letras: Array,
        verificarLetra: Function,
        jogar: Function
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
    .teclado {
        display: flex;
        flex-wrap:wrap;
        justify-content: center;
        width: 85%;
        margin-top: 20px;
    }

    .teclado-botao {
        text-transform: uppercase;
        margin: 5px;
    }
</style>