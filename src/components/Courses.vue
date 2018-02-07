<template lang='pug'>
  .section
      button(v-on:click='ver = !ver') mostrar/ocultar
      transition(name='transicion')
        h1(v-if='ver', v-text='mensaje.cursos')
      .section-contents
        .section-contents-info
          img(src='../assets/imagen1.jpg')
          h2 READING ONLINE E-BOOKS
          p Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s
        .section-contents-info
          img(src='../assets/imagen2.jpg')
          h2 ONLINE TUTORIAL WITH EXAMPLE
          p Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s
        .section-contents-info
          img(src='../assets/imagen3.jpg')
          h2 STUDY WITH EASE
          p Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s
      input(type='text' placeholder='Indroducir un curso')
      input(type='button' value='Enviar Tarea' v-on:click='AgregarTarea')
      //- pre{{data}}


</template>

<script>
export default {

  data(){
    return {
      ver: "true",
      mensaje: {
        cursos: 'COURSES WE OFFER ...'
      }
      
    }
  }
}
</script>

<style lang='scss'>
  .section{
    padding: 7em;
    & h1{
      text-align: center;
      padding-bottom: 2em;
      color: rgb(56, 69, 79);

    
    }

    .transicion-enter-active {
      transition: all 0.3s ease;
    }
    .transicion-leave-active {
      transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
    }
    .transicion-enter,
    .transicion-leave-to {
      transform: translateX(10px);
      opacity: 0;
    }

    &-contents{
      
      width: 100%;
      display: grid;
      grid-template-columns: repeat(3,1fr);
      grid-template-rows: 50%;
      // grid-template-columns: 30% 30% 30%;
      grid-column-gap: 2em;
      justify-items: center;
      // align-items: center;

      &-info{
        width: 100%;
        & h2{
          text-align: center;
          font-size: 16px;
          padding: 2em;

          &:after{
            content: '';
            background: rgb(134, 188, 66);
            text-align: center;
            display: block;
            width: 100px;
            height: 4px;
            margin-top: 2em;
            margin-right: auto;
            margin-left: auto;

          }
        }
        & p{
          text-align: center;
          line-height: 1.5em;
          color: rgb(56, 69, 79);
          font-size: 17px;
          
        }
        & img{
        width: 100%;
        height: auto;
        display: block;
        }

      }
    }
  }
</style>
