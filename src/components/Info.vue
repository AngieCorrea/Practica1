<template lang='pug'>
  .asider
      button(v-on:click='mirar=!mirar') mostrar/ocultar
      transition
        h1(v-if='mirar', v-text='ejemplo.transicion')
      .asider-info
        img(src='../assets/imagen4.png')
        transition(
          name="animacion"
          enter-active-class="animated fadeInLeft"
          leave-active-class="animated fadeOut" appear)
          p(v-if='mirar', v-text='ejemplo.animacion')
</template>

<script>
export default {

  data(){
    return{
      mirar: 'true',
      ejemplo: {
        transicion: 'WHAT WE OFFER',
        animacion: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.'
      }
    }
  }
  
}
</script>
