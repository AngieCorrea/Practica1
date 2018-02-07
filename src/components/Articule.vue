<template lang='pug'>
  .articule
      h1 OUR BLOG 
      .articule-container
        .articule-container-info
          img(src='../assets/imagen5.jpg')
          .fecha
            p 11 December, 2015
            p Lorem Ipsum Dummy Text
          h2 Difference of Education now-a-days
          p Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
          a READ MORE 
        .articule-container-info
          img(src='../assets/imagen6.jpg')
          .fecha
            p 11 December, 2015
            p Lorem Ipsum Dummy Text
          h2 Online Tutorial Sites help Learn easily
          p Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry’s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
          a READ MORE 
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
