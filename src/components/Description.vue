<template lang='pug'>
  .description#caracteristicas
      .description-info
        h2 50 +
        p CURSOS QUE OFRECEMOS
      .description-info
        h2 500 +
        p EJEMPLO TUTORIAL
      .description-info
        h2 200 +
        p MIEMBROS DEL EQUIPO EXPERTO
      .description-info
        h2 200 +
        p AÑOS DE EXPERIENCIA

</template>

<script>
export default {

}
</script>

<style lang='scss'>
  .description{
    background: rgb(36, 44, 66);
    width: 100%;
    display: grid;
    grid-template-columns: repeat(4,1fr);
    justify-items: center;
    align-content: center;
    padding: 4em 0;
    &-info{
     
     & h2{
       width: 100%;
       color: white;
       font-size: 2.5em;
       text-align: center;
       margin-bottom: .5em;
     }
     & p{
       text-align: center;
       color: white;
     }

    }
  }
</style>
