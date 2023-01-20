<template>
    <div class="container">
        <div class="content">
        <div class="portada text-center ">
        <div class="title ">
        <h1>Monumentos Cuba Game</h1>
        </div>
        <div class="botones">
        <button class=" btn-principal" @click="onPlay">Play</button>
        <button class=" btn-principal" @click="onAyuda">Ayuda</button>
        <button class=" btn-principal" @click="onAcercade">Acerca de</button>

        </div>
        </div>
        </div>
    </div>
</template>
<style>

.content{
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.portada{
    background-color: rgba(255, 255, 255, 0.3);
    padding: 20px;
    box-shadow: 0px 0px 9px 6px rgb(0 0 0 / 24%);
}
.title{
    margin-bottom: 60px;
}

.btn-principal{
    background-color: #d39e00;
    color: black;
    border-radius: .45rem;
    margin-bottom: .65rem;
    border: none;
    width: 70%;
    height: 50px;
    cursor: pointer;
}
</style>
<script>

    export default{
        methods: {
            onPlay() {
                this.$emit('play');
            },
            onAyuda(){
                this.$emit('ayuda');
            },
            onAcercade(){
                 this.$emit('acercade');
            }
        }
    }
</script>
