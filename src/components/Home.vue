<template lang='pug'>
  .container
    nav.nav 
      img.nav-logo(src='../assets/menulogo.png')
      ul.nav-item
        a.nav-link(href='#') Home
        a.nav-link(href='#') About Us
        a.nav-link(href='#') Features
        a.nav-link(href='#') Courses
        a.nav-link(href='#') Contact
    .main
      .main-info
        transition(name="aparecer" )
          h1(v-if='show',v-text='mensajes.transicion')
        transition(name='animacion' appear)
          p(v-if='mostrar', v-text='mensajes.animacion') 
        a(v-on:click='mostrar = !mostrar') LEARN MORE
   
</template>


<script>
import Features from "../components/Features";
import About from "../components/About";
export default {
  components: { Features,About },
  // name: 'app',
  data() {
    return {
      mostrar: "true",
      show: "true",
      mensajes: {
        transicion: "WE PROVIDE ONLINE COURSES",
        animacion:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book."
      }
    };
  }
  // data () {
  //   return {

  //   }
  // }
};
</script>





<style lang='scss'>
.nav {
  padding: 1.5em 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: fixed;
  top: 0;
  z-index: 100;
  width: 100%;
  background: white;

  &-logo {
    width: 12%;
  }

  &-item {
    padding: 1em;
  }

  &-link {
    padding: 1em;
    color: white;
    text-decoration: none;
    text-transform: uppercase;
    color: black;

    &:hover {
      color: rgb(134, 188, 66);
    }
  }
}

.main {
  background: yellow;
  margin-top: 6em;
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: url("https://pixabay.com/get/ea35b40d2af0053ed1534705fb0938c9bd22ffd41cb0194191f0c878af/adult-3052244_1920.jpg");
  background-position: center;
  background-repeat: no-repeat;

  &-info {
    background: rgba(255, 255, 255, 0.8);
    width: 50%;
    height: 55%;
    padding: 2em 5em;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;

    .aparecer-enter-active {
      transition: all 0.3s ease;
    }
    .aparecer-leave-active {
      transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
    }
    .aparecer-enter,
    .aparecer-leave-to {
      transform: translateX(10px);
      opacity: 0;
    }

    .animacion-enter-active {
      animation: animacion 0.5s;
    }
    .animacion-leave-active {
      animation: animacion 0.5s reverse;
    }
    @keyframes animacion {
      0% {
        transform: scale(0);
      }
      50% {
        transform: scale(1.5);
      }
      100% {
        transform: scale(1);
      }
    }

    & h1 {
      text-align: center;

      &:after {
        content: "";
        background: rgb(134, 188, 66);
        text-align: center;
        display: block;
        width: 100px;
        height: 4px;
        margin-top: 1em;
        margin-right: auto;
        margin-left: auto;
      }
    }
    & p {
      text-align: center;
      line-height: 2.5em;
      font-size: 17px;
    }

    & a {
      background: rgb(134, 188, 66);
      color: white;
      padding: 0.5em;
      border-radius: 1%;
      cursor: pointer;

      &:hover {
        background: rgb(56, 69, 79);
      }
    }
  }
}

* {
  border: 0;
  margin: 0;
}
</style>
