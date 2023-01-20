<template>
    <div class="container">
        <nav class="navbar">
            <div class="navbar-home" @click="onInicio()">
                <h4><font-awesome-icon icon="arrow-left" /></h4>
            </div>
        </nav>
        <div class="content">
        <div class="portada text-center ">
        <div class="title ">
        <h2>¿Que es Monumentos Cuba Game?</h2>
        <p>Monumentos Cuba Game es una app-web que nos brinda la manera de aprender y conocer más, de una forma interactiva sobre los objetos, construcciones, sitios y centros históricos que han sido declarados Monumento Nacional de Cuba.</p>
        <h2>Desarrollado por:</h2>
        <p>Javier Ceballo Perez  estudiante UCI</p>
        <h2>Referencias:</h2>
        <p>MonumentosCuba.apk</p>
        </div>
        </div>
        </div>
    </div>
</template>
<script>

    export default{
        methods: {
            onInicio() {
                this.$emit('inicio');
            },    
        }
    }
</script>