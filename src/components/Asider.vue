<template lang='pug'>
  .asider
      h1 DESARROLLA TUS HABILIDADES CON NOSOTROS
      .asider-info.asider2
        .info
          p  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum. 
          p Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
        .img.imagen
    
</template>

<script>
export default {
  
}
</script>

<style lang='scss'>
  .asider{
    margin: 8em;


    & h1{
      text-align: center;
    }
    &-info{
      display: grid;
      grid-template-columns: repeat(2,1fr);
      justify-content: center;
      align-items: center;
      padding-top: 3em;
      justify-items: center;
      & .img{
        width: 50%;
        height: 300px;
        margin: auto;
        background-image: url('http://demos.templatetoaster.com/educate/wp-content/uploads/sites/128/2016/03/108.png');
        background-repeat: none;
        background-position: center;
        background-size: cover;
        display: block;

      }
      & p{
        line-height: 1.9em;
        color: rgb(56, 69, 79);
      }
    }

    
    & .asider2{
     & .imagen{
      background-image: url('http://demos.templatetoaster.com/educate/wp-content/uploads/sites/128/2016/03/111.jpg');
      width: 80%;
      height: 400px;
     }

    }
  }

</style>
