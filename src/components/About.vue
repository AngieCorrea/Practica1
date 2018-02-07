<template lang='pug' > 
    h1 {{nombre}}
</template>


<script>
export default {
  props: ['nombre'],
  data(){
    return{
      autor: 'Angie Clariza'
    }

   
  }
}
</script>

<style>

</style>
