<template lang="">
       <div class="containerbg">
        <div class="content">
            <img src="../assets/IMG_1622.png" alt="Foto de perfil">
            <h1>Pedro Ponte</h1>
            <h3>Full-Stack Developer</h3>
        </div>
        <nav :class="{ 'sticky': isSticky }">
            <input type="checkbox" name="" id="check">
            <label for="check" class="checkbtn"><i class="fas fa-bars"></i></label>
            <ul>
                <li><a href="#">Pagina Inicial</a></li>
                <li><a href="#quemsoueu">Quem Sou Eu</a></li>
                <li><a href="#oquefaco">O que faço</a></li>
                <li><a href="#hobbies">Hobbies</a></li>
            </ul>
        </nav>
        <div class="bg"></div>
    </div>
    <div class="container-fluid corpo"  :class="{ 'corpo-sticky': isSticky }"  >
        <section class="row justify-content-center">
            <div class="col-10 " id="quemsoueu">
                <ViewQuemSoueu></ViewQuemSoueu>
            </div>
        </section>
         <section class="row justify-content-center">
            <div class="col-10 " id="oquefaco">
                <ViewOquefaco></ViewOquefaco>
            </div>
        </section>
        
        <section class="row justify-content-center">
            <div class="col-10 " id="hobbies">
                <ViewHobbies></ViewHobbies>
            </div>
        </section>
      

    </div>
    <ViewRodape></ViewRodape>
</template>
<script>
import ViewQuemSoueu from './ViewQuemSoueu.vue';
import ViewHobbies from './ViewHobbies.vue';
import ViewOquefaco from './ViewOquefaco.vue';
import ViewRodape from './ViewRodape.vue';


export default {
    name: 'ViewHome',
    components: {
        ViewQuemSoueu,
        ViewHobbies,
        ViewOquefaco,
        ViewRodape

    },
    data() {
    return {
      isSticky: false,
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (window.pageYOffset >window.innerHeight) {
        this.isSticky = true;
      } else {
        this.isSticky = false;
      }
    },
  },

}

</script>
<style >
.corpo {
    padding-top: 20px;
    padding-bottom: 20px;
}
.corpo-sticky {
    padding-top:120px;
    padding-bottom: 20px;
}

.containerbg {
    background-image: url('../assets/IMG_1041.JPG');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: 100vh;
    z-index: -1;
    margin: 0px;
    padding: 0px;
}
.bg {
    /* background-image: url('../assets/IMG_1041.JPG'); */
    background-color: rgba(0, 0, 0, 0.5);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: 100vh;
    z-index: 0;
    margin: 0px;
    padding: 0px;
}

.content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: white;
}

.content img {
    width: 160px;
    height: 160px;
    object-fit: cover;
    border-radius: 50%;
    object-position: top center;
}


nav {
    background-color: rgba(0, 0, 0, 0.5);
    position: absolute;
    bottom: 0;
    width: 100%;
}

nav ul {
    list-style-type: none;
    text-align: center;
    padding: 5px;
}

nav ul li {
    display: inline;
    margin: 0 20px;
}

nav ul li a {
    text-decoration: none;
    color: white;
}
.sticky {
  position: fixed;
  top: 0;
  width: 100%;
  height: 50px;
  background-color: rgba(0, 0, 0,0.8);

}
.checkbtn{
    font-size: 30px;
    color: white;
    float: inline-end;
    line-height: 50px;
    margin: 0px;
   cursor: pointer;
   display: none;
}
#check{
    display: none;
}
@media (max-width: 600px) {
    .checkbtn{
        display: block;
    }
    nav {
        position: fixed;
  top: 0;
  width: 100%;
  height: 50px;
  background-color: rgba(0, 0, 0,0.8);

      display: flex;
  font-size: 1.5rem;
  justify-content: center;
  align-items: center;

    }
   nav ul{
        position: fixed;
        width: 100%;
        height: 100vh;
        background-color: rgba(0, 0, 0,0.8);
        top: 50px;
        left: -100%;
        text-align: center;
        transition: all .5s;
      
    }
    nav ul li {
        display: block;
    }
    nav ul li a{
       font-size: 20px;
    }
    #check:checked ~ ul{
        left: 0;
        
    } 
}
</style>