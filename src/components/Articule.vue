<template lang='pug'>
  .articule
      h1 NUESTRO BLOG
      .articule-container
        .articule-container-info
          img(src='http://demos.templatetoaster.com/educate/wp-content/uploads/sites/128/2016/03/109.jpg')
          .fecha
            p 8 Febrero, 2018
            p Lorem Ipsum Dummy Text
          h2 Diferencia de educación ahora
          p Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
          a LEE MAS

        .articule-container-info
          img(src='http://demos.templatetoaster.com/educate/wp-content/uploads/sites/128/2016/03/110.jpg')
          .fecha
            p 8 Febrero, 2018
            p Lorem Ipsum Dummy Text
          h2 Los sitios de tutoriales en línea ayudan a aprender fácilmente
          p Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
          a LEE MAS
</template>

<script>
export default {
  
}
</script>

<style  lang='scss'>
  .articule{
    width: 100%;
    & h1{
      text-align: center;
      padding: 3em 0;
    }
    &-container{
      display: grid;
      grid-template-columns: repeat(2,1fr);
      grid-gap: 4em;
      padding: 0 7em;
        &-info{
          background: rgb(249, 249, 249);
          padding: 2em;
        & img{
          width: 100%;
          display: block;
          height: auto,
        }

        & .fecha{
          padding: 2em 0;
          display: flex;
          justify-content: space-between;

          & p{
            color: rgb(56, 69, 79); 
            font-style: italic;
            font-weight: bold;
          }
        }

        & h2{
          padding-bottom: 1em;
          color: rgb(56, 69, 79);
        }

        

        & p{
          margin: 0;
          line-height: 2em;
          color: rgb(56, 69, 79);
        }

        & a{
          background: rgb(134, 188, 66);
          color: white;
          display: inline-block;
          padding: .5em 1em;
          border-radius: 1%;
          margin: 2em 0;
        }

      }
    }
    
  }

  
</style>
