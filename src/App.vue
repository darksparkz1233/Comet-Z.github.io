<template>
    <div id="main">
    <!-- ! Load Screen Component: -->
    <div id="load-screen">
      <LoadScreen />
    </div>

    <v-toolbar 
      color="#141516" 
      elevation-12
      id="header"
    >
      <v-toolbar-title id="header__title">
        Coffee Time
      </v-toolbar-title>

      <!-- language switcher: -->
      <div id="header__lang-switch">
        <div class="header__lang-switch-container">
          <p>
            <router-link to="/en">
              <img class="uk-flag" src="./assets/united-kingdom.png">
            </router-link>
          </p> 
          
          <p>
            <router-link to="/ru">
              <img class="ru-flag" src="./assets/russia.png">
            </router-link>
          </p>         
        </div>
      </div>
    </v-toolbar>

  <!-- language display -->
    <router-view>

    </router-view>  
     
  </div>
</template>

<script>

import LoadScreen from './components/UI/loadscreen/LoadScreen.vue'

export default {
  name: 'App',
  components: {
    LoadScreen,
    
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Pacifico&display=swap");
@import url('https://fonts.googleapis.com/css2?family=Nunito&family=Pacifico&display=swap');

h1 {
  font-size: 20px;
  display: flex;
}
a {
  text-decoration: none;
  font-size: 25px;
}

.uk-flag,
.ru-flag {
  height: 30px;
}

.header__lang-switch-container {
  display: flex;
  justify-content: space-between;
  align-items: center;

  width: 80px;

  margin-left: 20px;
  margin-top: 10px;
}

#main {
  display: flex;
  flex-direction: column;

  background: #0B0B0C;
}

#header {
  display: flex;
  justify-content: space-evenly;
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
