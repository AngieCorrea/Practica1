<template lang='pug'>
  .contacts
      .contacts-info
        h1 CONTACTATE CON NOSOTROS
        p  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
        a(href='#contactos') CONTÁCTANOS
</template>

<script>
export default {
  
}
</script>

<style lang='scss'>
  .contacts{
    background-image: url('https://static.pexels.com/photos/262569/pexels-photo-262569.jpeg');
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: center;
    width: 100%;
    &-info{
      background: rgba(36, 44, 66,0.8);
      padding: 7em;
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      text-align: center;
      align-items: center;
  
      & h1{
        color: white;
      }

      & p{
        color: white;
        line-height: 2em;
        padding: 2em 0;
        font-size: 18px;
      }

     
      & a{
        background: rgb(134, 188, 66);
        text-decoration: none;  
        color: white;
        display: inline-block;
        padding: .5em;
        border-radius: 1%;
        cursor: pointer;
      }
    }
   
  }

</style>
