<template lang='pug'>
  .footer#contactos
      .img
      p.datos 2345 Lambayeque, PERÚ
      p.datos Télefono 987-654-321
      .iconos
        a(href='https://www.facebook.com/Clariza21c' target='_blank')
          icon(name='facebook')
        a(href='https://www.instagram.com/clariza21c/' target='_blank')
          icon(name='instagram')
        a(href='https://twitter.com/iniciarsesion' target='_blank')
          icon(name='twitter')
        a(href='https://accounts.snapchat.com/accounts/welcome' target='_blank')
          icon(name='snapchat')
        a(href='https://github.com/AngieCorrea' target='_blank')
          icon(name='github')
        
      p.info Diseñado por
        spam.spam Anlly Clariza Correa Cueva
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
    padding: 2em;
    height: 300px;
    justify-content: space-around;
    // align-content: space-between;
    & .img{
        background-image: url("http://demos.templatetoaster.com/educate/wp-content/themes/theme-00103/menulogo.png");
        background-repeat: no-repeat;
        background-position: center;
        display: block;
        width: 25%;
        height: 80px;
        background-color: #fff;

    }

    & .iconos{
      // display: flex;
      // justify-content: space-between;
      & .fa-icon{
        width: 40px;
        height: 40px;
        color: #fff;
        padding: .5em;
      }
    }

    
    & p{
      font-size: 1.2em;
    
    }

    & .datos{
      color:  white;
    }
    & .info{
        // padding-top: 2em;
        color: rgb(134, 188, 66);
        
      & .spam{
        color: white;
        padding-left: .5em;
      }
    }
  }
</style>
