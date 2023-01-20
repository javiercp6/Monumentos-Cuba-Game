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
        <h2>¿Cómo se juega Monumentos Cuba Game?</h2>
        <p>En cada nivel se presenta una imágen relacionada con un monumento nacional y cuatro opciones de nombres de monumentos nacionales. El juego consiste en eligir el nombre que se relacione con la imágen. Inicias el juego con 10 vidas, cada vez que elijas una opción incorrecta perderás 1 vida, si llegas a 0 vidas pierdes el juego. Si elijes la opción correcta avanzas de nivel.</p>
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