<template lang='pug'>
  .footer
      img(src='../assets/menulogo.png')
      p.datos 2345 Lambayeque, PERÚ
      p.datos Télefono 987-654-321
      p.info Diseñado por
        spam.spam Anlly Clariza....
</template>

<script>
export default {
  
}
</script>

<style lang='scss'>
  .footer{
    background: rgb(36, 44, 66);
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 3em;
    justify-content: space-between;
    & img{
      padding: .5em;
      color: white;
      background: white;
      margin-bottom: 1em;

    }


    & p{
      font-size: 1.2em;
    
    }

    & .datos{
      color:  white;
    }
    & .info{
        padding-top: 5em;
        color: rgb(134, 188, 66);
        
      & .spam{
        color: white;
        padding-left: .5em;
      }
    }
  }
</style>
