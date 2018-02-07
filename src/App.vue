<template lang='pug'>
  #app
    Home
    Courses
    Description
    Info
    Contact
    Articule
    Asider
    Footer
</template>




<script>
import Home from './components/Home'
import Description from './components/Description'
import Info from './components/Info'
import Contact from './components/Contact'
import Articule from './components/Articule'
import Asider from './components/Asider'
import Courses from './components/Courses'
import Footer from './components/Footer'

export default {
  components: {Home,Description,Info,Contact,Articule,Asider,Footer,Courses},

  name: 'app',
  data () {
    return {
   
    }
  }
}
</script>

