<template>
<!-- ! ENGLISH -->
  <div id="main">
     <div class="row coffee-row-1">
        <Cappuccino class="coffee-card " />
        <Mocha class="coffee-card"/>
        <Americano class="coffee-card"/>
        <Doppio class="coffee-card "/>
      </div>

      <div class="row coffee-row-2">
        <FlatWhite class="coffee-card"/>
        <Irish class="coffee-card"/>
        <Macchiato class="coffee-card"/>
        <Bicerin class="coffee-card"/>
      </div>
  </div>
</template>

<script>
import Cappuccino from '../components/Cappuccino/Cappuccino.vue'
import Americano from '../components/Americano/Americano.vue'
import Doppio from '../components/Doppio/Doppio.vue'
import FlatWhite from '../components/Flat White/FlatWhite.vue'
import Irish from '../components/Irish/Irish.vue'
import Macchiato from '../components/Macchiato/Macchiato.vue'
import Mocha from '../components/Mocha/Mocha.vue'
import Bicerin from '../components/Bicerin/Bicerin.vue'



export default {
  components:{
   Cappuccino,
    Americano,
    Doppio,
    FlatWhite,
    Irish,
    Macchiato,
    Mocha,
    Bicerin,
}
}
</script>

<style scoped>
  @import url("https://fonts.googleapis.com/css2?family=Pacifico&display=swap");
@import url('https://fonts.googleapis.com/css2?family=Nunito&family=Pacifico&display=swap');


#main {
  display: flex;
  flex-direction: column;

  background: #0B0B0C;
}

#header {
  display: flex;
  justify-content: space-around;
  align-items: center;  

  width: 100%;
}

#header__title {
  color: #FFF;
  font-size: 25px;
  font-family: Pacifico, cursive;
}

.row {
  display: flex;
  justify-content: space-evenly;
  padding: 1rem;
}

  .coffee-row-1 {
    padding-top: 1rem;
  }
  
  .coffee-card {
    padding-bottom: 1rem;
  }


/* lang switch */
#lang-switch {
  text-align: center;
  background: #2e2e2e;
  color: #FFF;
  padding: 5px;

  font-family: 'Nunito', sans-serif;
  font-weight: bold;

  border-radius: 8px;

  margin-left: 1rem;
}




/* RESPONSIVE AREA:  */
/* tablets: */
@media screen and (max-width: 1256px) {
  #main { }

  .row {
    display: grid;
    grid-template-columns: 2fr 2fr;
    column-gap: 5rem;

    padding-top: 2%;
    padding-right: 20%;
    padding-left: 20%;
  }
}

/* mobile: */
@media screen and (max-width: 730px) {
  #main {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .row {
    display: flex;
    flex-direction: column;
  }
}
</style>


