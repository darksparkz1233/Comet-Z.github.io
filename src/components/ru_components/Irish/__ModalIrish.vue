<template>
  <div id="root">
    <Transition name="modal">
      <div v-if="show" class="modal-mask">
        <div class="modal-wrapper">
          <div class="modal-container">
            <div class="modal-header">
              <slot name="header">
                <h2 class="header">
                   <button 
                        class="modal-close-btn" 
                        @click="$emit('close')"
                    >
                  <svg width="14" height="24" viewBox="0 0 14 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M0.939355 10.9393C0.353569 11.5251 0.353569 12.4749 0.939355 13.0607L10.4853 22.6066C11.0711 23.1924 12.0208 23.1924 12.6066 22.6066C13.1924 22.0208 13.1924 21.0711 12.6066 20.4853L4.12134 12L12.6066 3.51472C13.1924 2.92893 13.1924 1.97919 12.6066 1.3934C12.0208 0.807613 11.0711 0.807613 10.4853 1.3934L0.939355 10.9393ZM4.00002 10.5H2.00002V13.5H4.00002V10.5Z" fill="white"/>
                  </svg>

                </button>  
                    АЙРИШ ☕
                </h2>
                <v-divider />
              </slot>
            </div>
            <div class="modal-body">
                <!-- Main content here: -->
              <slot name="body">
                <!-- INGREDIENTS -->
                <div class="irish__ingredients-container">
                    <h3 class="header">Ингридиенты:</h3>
                        <ul class="irish__ingredients">
                            <li>
                                2 чайные ложки упакованного коричневого сахара, по вкусу.
                            </li>
                            <li>
                                4 унции крепкого горячего кофе.
                            </li>
                            <li>
                                11/2 унции ирландского виски.
                            </li>
                            <li>
                                1 унция густых сливок, слегка взбитых.
                            </li>
                        </ul>     
                </div>
                <hr class="break-line">
                <!-- // INGREDIENTS // -->

                <!-- STEP-BY-STEP GUIDE -->
                <div class="irish__guide-container">
                    <h3 class="irish__guide header">Пошаговая инструкция:</h3>
                    <div class="irish__guide-steps">
                        <div class="irish__guide-first">
                            <ol>
                                <li>Соберите ингредиенты</li>
                                <br>
                                <li> Поместите коричневый сахар в стакан для теплого ирландского кофе, кружку или другой термостойкий стакан. </li>
                                <br>
                                <li> Добавьте кофе и ирландский виски. </li>
                                <br>
                                <li> Мешайте, пока сахар не растворится. </li>
                                <br>
                                <li> Сверху выложите слегка взбитые густые сливки, медленно выливая их по тыльной стороне ложки. </li>
                                <br>
                                <li> Не перемешивайте. Вместо этого пейте ирландский кофе со сливками. Наслаждайтесь.</li>
                            </ol>
                        </div>

                       <hr class="break-line">

                       <div class="irish__guide-second">
                            
                       </div>
                    </div>
                </div>
                <!-- // STEP-BY-STEP GUIDE // -->
              </slot>
            </div>

            <div class="modal-footer">
                <!-- Modal footer here: -->
              <slot name="footer">
   
              </slot>
            </div>
          </div>
        </div>
      </div>
    </Transition>
  </div>
</template>




<script>
export default {
  props: {
    show: Boolean,
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Nunito&family=Pacifico&display=swap');

#root {
    font-family: 'Nunito',sans-serif;
    font-size: 35px;
    color: #fff;
}

.irish__ingredients {
    font-size: 17px;
    margin-left: 2.5rem;
}



.irish__guide-steps {
    display: flex;
    flex-direction: column;
    align-content: space-between;

    font-size: 25px;
}

.irish__guide-first {
    margin-left: 25px;
    font-size: 20px;
}
.irish__ingredients-container {
  /* margin-bottom: 1rem; */
}
</style>