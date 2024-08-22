<template>
  <div>
    <head>
      <link href="https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:wght@300;700&display=swap" rel="stylesheet">
    </head>
    <div class="hello">
      <div class="three-columns">
        <div class="column">
          <img alt="Vue logo" src="./img/Image-01.jpg" @click="openModal('./src/components/img/Image-01.jpg')">
        </div>
        <div class="column">
          <img alt="Vue logo" src="./img/Image-02.jpg" @click="openModal2('./img/Image-02.jpg')">
          <img class="img3" alt="Vue logo" src="./img/Image-03.jpg" @click="openModal3('./img/Image-03.jpg')">
        </div>
        <div class="column-right">
          <div class="up">
            <h2 class="comp_1_title">ANSWER YOUR BODY'S NEEDS</h2>
            <hr>
            <p class="paragraph1">
              The way ingredients are sourced affects the way we nourish our bodies. Author Mark Schatzer believes our body naturally develops an appetite for the food and the nutrients it needs to be healthy, but artificial
              flavorings are getting in the way. This can be reversed by focusing on high-quality ingredients and being mindful as your appetite guides you to consume according to your body's needs.
            </p>
          </div>
          <div class="down">
            <h3 class="be_mindful">BE MINDFUL</h3>
            <p class="paragraph2"><strong>Sourcing local or organic food is a good way to start being more mindful about what you're cooking and eating.</strong></p>
          </div>
        </div>
      </div>
      <!-- Modals -->
      <div v-if="isModalVisible" class="modal" @click="closeModal">
        <img src="./img/Image-01.jpg" class="modal-content" @click.stop>
      </div>
      <div v-if="isModalVisible2" class="modal" @click="closeModal">
        <img src="./img/Image-02.jpg" class="modal-content" @click.stop>
      </div>
      <div v-if="isModalVisible3" class="modal" @click="closeModal">
        <img src="./img/Image-03.jpg" class="modal-content" @click.stop>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    // check status to hide or show modal
    return {
      isModalVisible: false,
      isModalVisible2: false,
      isModalVisible3: false,
      currentImage: ''
    };
  },
  methods: {
    //methods for the modal
    openModal(imageSrc) {
      this.currentImage = imageSrc;
      this.isModalVisible = true;
    },
    openModal2(imageSrc) {
      this.currentImage = imageSrc;
      this.isModalVisible2 = true;
    },
    openModal3(imageSrc) {
      this.currentImage = imageSrc;
      this.isModalVisible3 = true;
    },
    closeModal() {
      this.isModalVisible = false;
      this.isModalVisible2 = false;
      this.isModalVisible3 = false;
      this.currentImage = '';
    }
  }
}
</script>


<style scoped>
.hello {
  background-color: #0e0e0e;
  padding: 130px 100px 100px 140px;
}

.three-columns {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap; /* Allows columns to wrap on smaller screens */
}

.column, .column-right {
  flex: 1;
  padding: 10px;
  box-sizing: border-box;
}

.img3 {
  margin-top: 15px;
}

.down {
  text-align: left;
}

h2 {
  font-size: 26px;
}

h3 {
  font-size: 15px;
  color: red;
}

.be_mindful {
  font-family: 'Open Sans Condensed', sans-serif;
  font-weight: 400;
  letter-spacing: 0.08em;
  font-size: 20px;
}

.paragraph1, .paragraph2 {
  text-align: left;
  font-size: 20px;
  line-height: 1.5;
}

.column-right {
  display: flex;
  flex-direction: column;
  gap: 18px;
  margin-top: -15px;
}

.comp_1_title {
  width: 100%;
  font-family: 'Open Sans Condensed', sans-serif;
  font-weight: 400;
  text-align: left;
  letter-spacing: 0.08em;
  font-size: 30px;
}

.paragraph1 {
  font-family: 'Open Sans Condensed', sans-serif;
  font-size: 19px;
  line-height: 1.5;
  font-weight: 400;
  letter-spacing: 0.1em;
}

.paragraph2 {
  font-family: 'Open Sans Condensed', sans-serif;
  font-size: 19px;
  line-height: 1.5;
  font-weight: 300;
  letter-spacing: 0.01em;
}
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  max-width: 90%;
  max-height: 90%;
  border: 2px solid white;
}

.modal img {
  cursor: pointer;
}

/* Responsive adjustments for modal */
@media (max-width: 768px) {
  .modal-content {
    max-width: 80%;
    max-height: 80%;
  }
}

/* Responsive Design */
@media (max-width: 1024px) {
  .hello {
    padding: 100px 50px 50px 50px;
  }
  
  .three-columns {
    flex-direction: column;
  }
  
  .column, .column-right {
    width: 100%;
  }

  h2, .comp_1_title {
    font-size: 24px;
  }

  h3, .be_mindful {
    font-size: 18px;
  }

  .paragraph1, .paragraph2 {
    font-size: 16px;
  }
}

@media (max-width: 768px) {
  .hello {
    padding: 70px 20px 20px 20px;
  }
  
  h2, .comp_1_title {
    font-size: 22px;
  }

  h3, .be_mindful {
    font-size: 16px;
  }

  .paragraph1, .paragraph2 {
    font-size: 14px;
  }

  .down {
    margin-top: 20px;
  }
}

@media (max-width: 480px) {
  .hello {
    padding: 50px 10px 10px 10px;
  }
  
  h2, .comp_1_title {
    font-size: 20px;
  }

  h3, .be_mindful {
    font-size: 14px;
  }

  .paragraph1, .paragraph2 {
    font-size: 12px;
  }

  .img3 {
    margin-top: 10px;
  }
}
</style>
