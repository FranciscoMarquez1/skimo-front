<template>
    <div class="cardCustom">
        <p class="id"> {{cliente.id}} </p>
        <b-row align-v="center">
            <b-col cols="4">
                <b-img center :src="cliente.image_url"></b-img>
            </b-col>
            <b-col cols="8">
                <p class="clientName"> {{cliente.name}} </p>
            </b-col>
        </b-row>
        <a :href="'mailto:' + this.email" class="email">{{ this.email }}</a>
    </div>
</template>

<script>
    export default {
        name: 'Cliente',
        props: {
            cliente: Object
        },
        computed: {
            email() {
                return this.cliente.name.split(" ")[0] + "@example.com"; 
            }
        },
    }
</script>

<style scoped>
.cardCustom {
    padding: 15px;
    -webkit-border-radius: 12px; 
    border-radius: 10%;
    box-shadow: 0 0 2px 0px;
    margin: 20px 0px;
    max-width: 420px;
}

.id {
    color: #bebebe;
    text-align: right;
}

.email {
    display: block;
    text-align: right;
    font-weight: bold;
}
img {
    border-radius: 100%;
    width: 70%;
}

.clientName {
    font-size: 1.5rem;
    font-weight: bold;
    min-height: 72px;
}
</style>