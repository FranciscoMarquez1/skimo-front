<template>
    <div id="clientes-frecuentes">
        <h2>Clientes Frecuentes</h2>
        <b-row>
            <b-col cols="12" md="6"  v-for="cliente in apidata" :key="cliente.index" >
                    <Cliente class="cliente" :cliente="cliente"/>
            </b-col>
        </b-row>

    </div>
</template>

<script>
import axios from 'axios';
import Cliente from './Cliente'

    export default {
        name: 'ClientesFrecuentes',
        components: {
            Cliente
        },
        data() {
            return {
                apidata: []
            }
        },
        mounted () {
            axios
            .get('https://api.jsonbin.io/b/605295617ea6546cf3e18655')
            .then(response => (this.apidata = response.data))
            .catch(error => console.log(error));
        },
    }
</script>

<style scoped>
    #clientes-frecuentes {
        text-align: left;
        padding-left: 3em;
    }
    h2 {
        font-weight: 700;
        margin-bottom: 2rem;
    }

    @media (max-width: 768px) {
        #clientes-frecuentes {
            padding-left: 0px;
        }
    }
</style>