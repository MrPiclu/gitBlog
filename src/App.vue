<template>
    <div>
      <div class="backGroundColor" :class="{backGroundColor2 : changeColor}">
      </div>

      <div style="position: absolute;">

        <span class="sideimg" :class="{sideimg2 : changeColor}">

          <div class="sideBlock">
            <img class="headimg" alt="Vue logo" src="./assets/frieren.jpg">
          </div>
          <div>
            <button @click="changeColor1()"><h1>change Color</h1></button>
          </div>
          
        </span>
        
        <span style="width: 84vw; height: 100vh; float: left;">
            <h1>Welcome to my Blog!!!!!!!</h1>

        </span>

      </div>


    </div>

</template>

<script>

import {ref} from 'vue'

export default {
  name: 'App',
  setup(){
    const changeColor = ref(true)

    const changeColor1 = () => {
      changeColor.value = !changeColor.value;
    }

    return {
      changeColor,
      changeColor1
    }
  },
  data(){
    return{
    }
  },
  methods: {
    
  },
}
</script>

<style>
body{
  padding: 0;
  margin: 0;
  height: 100%;
  top: 0;
  left: 0;
}

#app {
  top: 0;
  left: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /* color: #2c3e50; */

  /* animation: backGroundAnimation linear 5s infinite; */
  /* animation-direction: alternate; */
}

.backGroundColor{
  background: linear-gradient(382deg, #1a4249, #211290db, #769a98); 
  position: absolute; 
  height: 100%; 
  width: 100%;
  animation: backGroundAnimation linear 5s infinite;
  animation-direction: alternate;

}
.backGroundColor2{
  background: linear-gradient(230deg, #56a55a, #627558, #235439);
  position: absolute; 
  width: 100%;
  animation: backGroundAnimation linear 5s infinite;
  animation-direction: alternate;

}

.sideBlock{
  height: 80%;
}

.headimg{
  background-color: black;
  width: 100%;
}

.sideimg{
  float: left;
  width: 16vw;
  height: 100vh;
  background-color: rgba(34, 48, 76, 0.929);
}
.sideimg2{
  float: left;
  width: 16vw;
  height: 100vh;
  background-color: rgba(24, 76, 53, 0.934);
}


.backGroundAnimation {
  animation: backGroundAnimation linear 5s infinite;
  animation-direction: alternate;
}

@keyframes backGroundAnimation {
    0%{background-size: 100%;
     }
    100%{background-size: 260%;
    }
}

@keyframes transition {
    0%{opacity: 1;
     }
    100%{opacity: 0;
    }
}

</style>
