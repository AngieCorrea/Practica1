
<template lang='pug'>
  .container
    h1 {{message}}
    .contendedor
      input(type='search' ,v-model='busqueda' ,placeholder='buscar')
      ul
        li(v-for='juego in buscarJuego') {{ juego.titulo }}
      ul
        li(v-for='juego in juegos') {{ juego.titulo }}
      input(type='range',min='0',max='10',v-model='minimo')
      form(v-on:submit.prevent='agregarTarea')
        input(type='text' placeholder='Ingresar Curso' v-model='nuevaTarea')
        input(type='submit' value='Enviar curso' )  
    
    //- h1(v-if='ganador') El ganador es : {{ganador}}
    //- template(v-else)
    //-   h1 Participantes
    //-   ul
    //-     li(v-for='persona in listado') {{persona}}
    //- button(@click='elegirGanador' ) Elegir ganador

  
</template>



<script>

export default {
// props: ['listado'],
  data() {
  
    return {
      autor:'Angie Clariza',
      message: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry",
      mensaje: "holaaaaaaaaaaaaaaaaaaaa",
      nuevaTarea: null,
      tareas: ["Aprender Vue.js", "Aprender ES6"],
      busqueda:' ',
      minimo: 5,
      juegos: [
        {
          titulo: "Battlefield",
          genero: "FPS",
          puntuacion: 4
        },
        {
          titulo: "civilization vi",
          genero: "estrategia",
          puntuacion: 10
        },
        {
          titulo: "resident evil 7",
          genero: "survival horror",
          puntuacion: 7
        }
      ],
      // ganador: false,
      // participantes: this.listado,
      // personas: ['Juan', 'Alicia', 'Pedro', 'Javier', 'Marcos']
    };
  },

  // props:['nombre'],

  methods: {
    agregarTarea() {
      this.tareas.unshift(this.nuevaTarea);
      this.nuevaTarea = "";
    }
  },

  // methods:{
  //   elegirGanador(){
  //     let cantidad= this.participantes.length;
  //     let indice=Math.floor((Math.random()*cantidad));
  //     this.ganador=this.participantes[indice-1];
  //   }
  // },

  computed:{
    mejoresJuegos(){
      return this.juegos.filter((juego)  => juego.puntuacion >= this.minimo);
    },
    buscarJuego(){
      return this.juegos.filter((juego) => juego.titulo.includes(this.busqueda));
    }
  },

 
};
</script>

<style>

</style>
