<template lang='pug'>
  div.contanier
    h1 hola mundo
    input(type='text' v-model='tarea')
    label 
      input(type='radio' v-model='autor' value='Angie' name='autor')
      | Angie
    label
      input(type='radio' v-model='autor' value='Clariza' name='autor')
      | Clariza
    br
    button(v-on:click='agregarTarea') Agregar
    h2(v-if='listaTareas.length>0') Mis tareas
    ul
      li(v-for='mitarea in listaTareas' @click='cambiarEstado(mitarea)' :class="{trealizada : mitarea.hecho}") {{mitarea.tarea}} - {{mitarea.autor}}
    h2(v-if='tareasRealizadas.length>0') Tareas Realizadas
    ul
      li(v-for='trealizada in tareasRealizadas')  {{trealizada.tarea}}-{{trealizada.autor}}
    h2(v-if='tareasDeAngie.length>0') Tareas de Angie
    ul
      li(v-for='trealizada in tareasDeAngie')  {{trealizada.tarea}}
    pre {{$data}}
</template>

<script>
export default {
  data(){
    return{
      autor: '',
      tarea:'',
      listaTareas: [],
      tareasRealizadas:[]
    }
  },

  methods:{
    agregarTarea(){
      this.listaTareas.push({
            tarea: this.tarea,
            autor: this.autor,
            hecho: false
        });
        this.tarea='';
        this.getTaskDone();
    },
    cambiarEstado(tarea){
      let i = this.listaTareas.indexOf(tarea);
      tarea.hecho=!tarea.hecho;
      this.listaTareas[i]=tarea;
      this.getTaskDone();
    },
    getTaskDone(){
      this.tareasRealizadas = this.listaTareas.filter(val=>val.hecho);
    }
  },

  computed:{
    tareasDeAngie(){
      return this.listaTareas.filter(val=>val.autor=='Angie')
    }
  }

}
</script>

<style>
  .trealizada{
    color: brown;
  }
</style>
