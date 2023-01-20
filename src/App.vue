<template>
    <div class="container-inicio">
                
                <transition name="flip" mode="out-in">
                     <component :is="mode" @inicio="mode = 'app-inicio'"  @play="mode = 'app-question'" @ayuda="mode = 'app-ayuda'" @acercade="mode = 'app-acercade'"></component>       
                </transition>   
        
    </div>
</template>

<script>
    import Question from './components/Question.vue';
    import Inicio from './components/Inicio.vue';
    import Ayuda from './components/Ayuda.vue';
    import Acercade from './components/Acercade.vue';
    
    

    export default {
        data() {
            return {
                pregunta: false,
                inicio: true,
                mode: 'app-inicio'
            }
        },
        methods: {

            play(){
               this.pregunta = true 
               this.inicio = false
            },

             

          /*answered(isCorrect) {
              if (isCorrect) {
                  this.mode = 'app-answer';
              } else {
                  this.mode = 'app-question';
                  alert('Wrong, try again!');
              }
          },*/

          
               
        },
        components: {
            appQuestion: Question,
            appInicio: Inicio,
            appAyuda: Ayuda,
            appAcercade: Acercade
            
            
        },
       
        
    }
</script>

<style>

body{
    width: 100%;
    height: 100vh;
    background-color: #d39e00 !important;
}
    
    /*.flip-enter {
        transform: rotateY(0deg);
    }*/
    

    .flip-enter-active {
        animation: flip-in  0.5s ease-out forwards;
    }
   /* .flip-leave {
        transform: rotateY(0deg);
    }*/

    .flip-leave-active {
        animation: flip-out 0.5s ease-out forwards;
    }

    @keyframes flip-out {
        from {
            transform: rotateY(0deg);
        }
        to {
            transform: rotateY(90deg);
        }
    }

    @keyframes flip-in {
        from {
            transform: rotateY(90deg);
        }
        to {
            transform: rotateY(0deg);
        }
    }
</style>
